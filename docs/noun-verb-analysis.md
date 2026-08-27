Manu Dev(20251501104)
Aditya Ukey(20251501011)
B Sai Ganesh Reddy(20251501049)    
Sathwik Gattu(20251501067)
Basa Jagan(20251501038)


## Smart Tourist Guide & Trip Planner

## 1. Noun–Verb Analysis

For this part, I analyzed the three given use-case specifications and first listed the important nouns and verbs. After that, I checked the nouns using four filters to decide which ones can be considered as classes.

The four filters used are:

1. **Redundancy:** Remove nouns that mean the same thing as another noun.
2. **Attribute:** Remove nouns that are better treated as attributes of another class.
3. **Operation:** Remove nouns that actually represent an action or process.
4. **Outside Scope:** Remove nouns that belong to an external system.

---

## 1.1 Plan Trip Itinerary

### Raw Nouns

The main nouns found in this specification are:

* Tourist
* User
* Destination
* Travel Time
* Preference
* Tourist Place
* Location
* Route
* Travel Information
* AI / LLM Recommendation Engine
* Itinerary
* Order
* Distance
* Suggestion
* System
* Weather Information
* Weather API

### Raw Verbs

The main verbs are:

* Login
* Select
* Enter
* Search
* Retrieve
* Send
* Generate
* Optimize
* Display
* Review
* Accept
* Inform
* Change
* Suggest

### Filtering the Nouns

| Noun                           | Result | Filter        | Reason                                               |
| ------------------------------ | ------ | ------------- | ---------------------------------------------------- |
| Tourist                        | Keep   | -             | Main person using the system                         |
| User                           | Remove | Redundancy    | Same as Tourist                                      |
| Destination                    | Keep   | -             | A place the tourist wants to visit                   |
| Travel Time                    | Remove | Attribute     | Can be stored as itinerary/route information         |
| Preference                     | Keep   | -             | Stores what the tourist is interested in             |
| Tourist Place                  | Remove | Redundancy    | Same idea as Destination                             |
| Location                       | Remove | Attribute     | Can be stored as destination/route information       |
| Route                          | Keep   | -             | Needed for travelling between places                 |
| Travel Information             | Remove | Attribute     | General information related to route and travel time |
| AI / LLM Recommendation Engine | Remove | Outside Scope | External system                                      |
| Itinerary                      | Keep   | -             | Main trip plan created by the system                 |
| Order                          | Remove | Attribute     | Part of the itinerary                                |
| Distance                       | Remove | Attribute     | Can be an attribute of Route                         |
| Suggestion                     | Remove | Operation     | It is a result of recommendation                     |
| System                         | Remove | Outside Scope | The system itself is not a domain class              |
| Weather Information            | Keep   | -             | Can affect the trip plan                             |
| Weather API                    | Remove | Outside Scope | External system                                      |

### Classes Surviving from Specification 1

* Tourist
* Destination
* Preference
* Route
* Itinerary
* WeatherInformation

---

## 1.2 Book Trip Services

### Raw Nouns

* Tourist
* Hotel
* Transportation
* Service
* Payment Gateway
* Service Provider
* Booking
* Service Details
* Price
* Booking Information
* Availability
* Payment Request
* Payment
* Confirmation
* Payment Method

### Raw Verbs

* Select
* Display
* Provide
* Verify
* Confirm
* Send
* Process
* Receive
* Create
* Inform
* Retry
* Choose

### Filtering the Nouns

| Noun                | Result | Filter        | Reason                                    |
| ------------------- | ------ | ------------- | ----------------------------------------- |
| Tourist             | Keep   | -             | Person making the booking                 |
| Hotel               | Remove | Redundancy    | Can be treated as a type of Service       |
| Transportation      | Remove | Redundancy    | Can be treated as a type of Service       |
| Service             | Keep   | -             | Represents a hotel or transport service   |
| Payment Gateway     | Remove | Outside Scope | External system                           |
| Service Provider    | Keep   | -             | Provides the service                      |
| Booking             | Keep   | -             | Stores the booking made by the tourist    |
| Service Details     | Remove | Attribute     | Details belong to Service                 |
| Price               | Remove | Attribute     | Price can be stored in Service            |
| Booking Information | Remove | Attribute     | Information belongs to Booking            |
| Availability        | Remove | Attribute     | Can be stored as part of Service          |
| Payment Request     | Remove | Operation     | It is part of the payment process         |
| Payment             | Keep   | -             | Represents the payment made for a booking |
| Confirmation        | Remove | Operation     | It is the result of the booking process   |
| Payment Method      | Remove | Attribute     | Can be stored inside Payment              |

### Classes Surviving from Specification 2

* Tourist
* Service
* ServiceProvider
* Booking
* Payment

---

## 1.3 Dynamic Itinerary Adjustment

### Raw Nouns

* Tourist
* Itinerary
* Weather API
* Weather Information
* Map / Location API
* Route Information
* AI / LLM Recommendation Engine
* Alternative Itinerary
* Scheduler
* Weather Conditions
* Destination
* Route
* Suggestion
* Change
* Alternative Destination

### Raw Verbs

* Check
* Receive
* Identify
* Retrieve
* Generate
* Create
* Display
* Review
* Accept
* Search
* Modify
* Postpone
* Remove
* Recommend

### Filtering the Nouns

| Noun                           | Result | Filter        | Reason                                         |
| ------------------------------ | ------ | ------------- | ---------------------------------------------- |
| Tourist                        | Keep   | -             | User of the system                             |
| Itinerary                      | Keep   | -             | Existing trip plan that may need changes       |
| Weather API                    | Remove | Outside Scope | External system                                |
| Weather Information            | Keep   | -             | Used to check whether weather affects the trip |
| Map / Location API             | Remove | Outside Scope | External system                                |
| Route Information              | Remove | Redundancy    | Already represented by Route                   |
| AI / LLM Recommendation Engine | Remove | Outside Scope | External system                                |
| Alternative Itinerary          | Remove | Redundancy    | Still an Itinerary                             |
| Scheduler                      | Remove | Outside Scope | Implementation detail                          |
| Weather Conditions             | Remove | Attribute     | Part of WeatherInformation                     |
| Destination                    | Keep   | -             | Destination may be affected by weather         |
| Route                          | Keep   | -             | Alternative route may be required              |
| Suggestion                     | Remove | Operation     | Result of recommendation                       |
| Change                         | Remove | Operation     | Represents an action/state change              |
| Alternative Destination        | Remove | Redundancy    | Still a Destination                            |

### Classes Surviving from Specification 3

* Tourist
* Itinerary
* WeatherInformation
* Destination
* Route

---

## 1.4 Final Classes

After combining the results from all three specifications and removing duplicate classes, the final classes are:

1. Tourist
2. Destination
3. Itinerary
4. Preference
5. Route
6. WeatherInformation
7. Service
8. ServiceProvider
9. Booking
10. Payment

