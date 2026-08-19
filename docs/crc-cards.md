Manu Dev(20251501104)
Aditya Ukey(20251501011)
B Sai Ganesh Reddy(20251501049)    
Sathwik Gattu(20251501067)
Basa Jagan(20251501038)







# 2. CRC Cards

## 2.1 Tourist

| Class                | Tourist                                                                              |
| -------------------- | ------------------------------------------------------------------------------------ |
| **Responsibilities** | Login, select destinations, give preferences, plan trip, book services, make payment |
| **Collaborators**    | Destination, Preference, Itinerary, Booking, Payment                                 |

---

## 2.2 Destination

| Class                | Destination                                          |
| -------------------- | ---------------------------------------------------- |
| **Responsibilities** | Store destination details, provide place information |
| **Collaborators**    | Itinerary, Route, WeatherInformation                 |

---

## 2.3 Itinerary

| Class                | Itinerary                                                                |
| -------------------- | ------------------------------------------------------------------------ |
| **Responsibilities** | Create trip plan, arrange destinations, optimize route, update itinerary |
| **Collaborators**    | Tourist, Destination, Preference, Route, WeatherInformation              |

---

## 2.4 Preference

| Class                | Preference                                 |
| -------------------- | ------------------------------------------ |
| **Responsibilities** | Store interests, available time and budget |
| **Collaborators**    | Tourist, Destination, Itinerary            |

---

## 2.5 Route

| Class                | Route                                 |
| -------------------- | ------------------------------------- |
| **Responsibilities** | Store route, distance and travel time |
| **Collaborators**    | Destination, Itinerary                |

---

## 2.6 WeatherInformation

| Class                | WeatherInformation                                         |
| -------------------- | ---------------------------------------------------------- |
| **Responsibilities** | Store weather details, provide updated weather information |
| **Collaborators**    | Destination, Itinerary                                     |

---

## 2.7 Service

| Class                | Service                                               |
| -------------------- | ----------------------------------------------------- |
| **Responsibilities** | Store hotel/transport details, price and availability |
| **Collaborators**    | ServiceProvider, Booking                              |

---

## 2.8 ServiceProvider

| Class                | ServiceProvider                                                 |
| -------------------- | --------------------------------------------------------------- |
| **Responsibilities** | Provide services, provide service details, confirm availability |
| **Collaborators**    | Service, Booking                                                |

---

## 2.9 Booking

| Class                | Booking                                                          |
| -------------------- | ---------------------------------------------------------------- |
| **Responsibilities** | Create booking, store booking details, confirm or cancel booking |
| **Collaborators**    | Tourist, Service, ServiceProvider, Payment                       |

---

## 2.10 Payment

| Class                | Payment                                                       |
| -------------------- | ------------------------------------------------------------- |
| **Responsibilities** | Process payment, store payment details, verify payment status |
| **Collaborators**    | Booking                                                       |
