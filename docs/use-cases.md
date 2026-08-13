# Use Case Specifications

## Use Case 1: Plan Trip Itinerary

**Primary Actor:** Tourist / User

**Stakeholders:**
- Tourist / User: Wants a suitable and organized travel plan.
- AI / LLM Recommendation Engine: Helps generate relevant itinerary suggestions.
- Map / Location API: Provides route and travel information.
- Weather API: Provides weather information that may affect the plan.

**Preconditions:**
- The tourist is registered and logged in.
- The tourist has selected a destination.
- Required destination and location information is available.

**Postconditions:**
- A suitable itinerary is generated and displayed to the tourist.
- The itinerary contains selected places in a practical order.
- Estimated travel time and route information are provided.

**Trigger:**
The tourist selects the option to plan a trip and provides the destination, available time, and preferences.

### Main Flow

1. The tourist logs into the system.
2. The tourist selects a destination.
3. The tourist enters available travel time and preferences.
4. The system searches for relevant tourist places.
5. The system retrieves location, route, and travel-time information.
6. The system sends the relevant information to the AI / LLM Recommendation Engine.
7. The system generates a suitable itinerary.
8. The system optimizes the order of destinations based on available time and travel distance.
9. The system displays the itinerary to the tourist.
10. The tourist reviews and accepts the itinerary.

### Alternate Flows

**A1. No suitable places found**
1. The system cannot find enough suitable places for the selected destination.
2. The system informs the tourist.
3. The tourist changes the destination or preferences.
4. The system searches again.

**A2. Insufficient available time**
1. The selected places cannot reasonably fit within the available time.
2. The system informs the tourist.
3. The system suggests fewer or closer destinations.
4. The tourist accepts the suggested itinerary or modifies the preferences.

---

## Use Case 2: Book Trip Services

**Primary Actor:** Tourist / User

**Stakeholders:**
- Tourist / User: Wants to book required hotel or transportation services.
- Payment Gateway: Processes the payment securely.
- Service Provider: Receives and confirms the booking.

**Preconditions:**
- The tourist is logged in.
- The tourist has selected a service such as a hotel or transportation.
- The selected service is available.

**Postconditions:**
- The booking is successfully created.
- Payment is processed.
- The tourist receives booking confirmation.

**Trigger:**
The tourist selects an available hotel or transportation service and chooses to book it.

### Main Flow

1. The tourist selects a hotel or transportation service.
2. The system displays the service details and price.
3. The tourist provides the required booking information.
4. The system verifies service availability.
5. The tourist confirms the booking.
6. The system sends the payment request to the Payment Gateway.
7. The Payment Gateway processes the payment.
8. The system receives successful payment confirmation.
9. The system creates the booking.
10. The system displays the booking confirmation to the tourist.

### Alternate Flows

**A1. Service is unavailable**
1. The system checks availability.
2. The selected service is no longer available.
3. The system informs the tourist.
4. The tourist selects another available service.

**A2. Payment fails**
1. The Payment Gateway rejects or fails to process the payment.
2. The system informs the tourist that the payment was unsuccessful.
3. The booking is not confirmed.
4. The tourist can retry the payment or choose another payment method.

---

## Use Case 3: Dynamic Itinerary Adjustment

**Primary Actor:** Tourist / User

**Stakeholders:**
- Tourist / User: Wants the trip plan to remain practical and safe.
- Weather API: Provides updated weather information.
- Map / Location API: Provides updated route and travel information.
- AI / LLM Recommendation Engine: Helps generate an alternative itinerary.

**Preconditions:**
- The tourist already has an active itinerary.
- Weather information is available.
- The system can access updated destination and route information.

**Postconditions:**
- The itinerary is updated if the weather change significantly affects the trip.
- Alternative destinations or routes are suggested.
- The tourist receives the updated itinerary.

**Trigger:**
The system detects that weather conditions have changed significantly and may affect the current itinerary.

### Main Flow

1. The Scheduler or system checks updated weather information.
2. The system receives new weather information from the Weather API.
3. The system identifies that the weather has changed significantly.
4. The system checks the destinations affected by the weather.
5. The system retrieves alternative destinations and routes.
6. The AI / LLM Recommendation Engine generates alternative suggestions.
7. The system creates an adjusted itinerary.
8. The system displays the changes to the tourist.
9. The tourist reviews and accepts the updated itinerary.

### Alternate Flows

**A1. Weather change does not affect the itinerary**
1. The system receives updated weather information.
2. The system determines that the current destinations are still suitable.
3. No itinerary changes are made.
4. The tourist continues with the existing itinerary.

**A2. No suitable alternative destination is available**
1. The system identifies that a planned destination is unsuitable.
2. The system searches for alternatives.
3. No suitable alternative is found within the available time and location.
4. The system informs the tourist and recommends postponing or removing the affected destination.
5. The tourist decides whether to modify the itinerary manually.