erDiagram
    User {
        int UserID PK
        varchar Username
        varchar Email
        blob ProfilePic
        varchar PhoneNumber
        text Address
        varchar FirstName
        varchar LastName
        Date DOB
        boolean VerifiedEmail
        boolean VerifiedPhoneNumber
        varchar ProfilePhoto
    }
    
    UserBehavior {
        int BehaviorID PK
        int UserID FK
        varchar RideStatus
        varchar CycleMaintenanceStatus
        varchar CycleStatus
        int Rating
    }
    
    UserStatus {
        int StatusID PK
        int UserID FK
        int CurrentRideID FK
        varchar Status
        timestamp LastActive
    }
    
    IncidentReport {
        int IncidentID PK
        int UserID FK
        int CycleID FK
        varchar IncidentType
        text Description
        timestamp ReportTime
        varchar Status
        int ResponseTeamID FK
        text ResolutionDetails
        timestamp ResolutionTime
        float IncidentLatitude
        float IncidentLongitude
    }
    
    ResponseTeam {
        int ResponseTeamID PK
        varchar TeamName
        varchar ContactNumber
        varchar Email
        boolean Available
        int TeamLeaderID FK
        varchar TeamLeaderProfilePhoto
        float TeamLatitude
        float TeamLongitude
    }
    
    CycleType {
        int TypeID PK
        varchar TypeDesc
    }
    
    Cycle {
        int CycleID PK
        int StationID FK
        varchar CycleName
        int CycleTypeID FK
        varchar Status
    }
    
    CycleStation {
        int StationID PK
        varchar StationName
        varchar StationAddress
        float Longitude
        float Latitude
        int OwnerID FK
        varchar Description
        varchar WebsiteUrl
        json SocialLinks
        varchar ContactNo
        json Thumbnails
    }
    
    ReviewRating {
        int RatingID PK
        int RatingRate
        varchar comment
        int RatingOrderReference
        int RatingCycleStation FK
    }
    
    Booking {
        int BookingID PK
        int UserID FK
        int CycleStationID FK
        decimal TotalAmount
        varchar BookingStatus
        datetime BookingDate
    }
    
    Trip {
        int TripID PK
        int UserID FK
        varchar Status
        int StartStationID FK
        int StopStationID FK
        float Price
        varchar Distance
        varchar Duration
        int StationManagerID FK
        timestamp StartTime
        timestamp StopTime
    }
    
    TripCycles {
        int TripID FK
        int CycleID FK
        date DateReturned
         
    }
    
    Chat {
        int ChatID PK
        int PassengerID FK
        int StationManagerID FK
        int TripID FK
        varchar Content
        timestamp CreatedAt
        timestamp UpdatedAt
    }
    
    RentalCharge {
        int RentalChargeID PK
        int CycleTypeID FK
        varchar ChargeType
        decimal AmountPerHour
        decimal AmountPerDay
        decimal AmountPerMin
        int MinimumHour
        int MinimumPrice
    }
    
    Subscription {
        int SubscriptionID PK
        int StationManagerID FK
        varchar SubscriptionType
        decimal AmountPerCycle
        decimal PercentagePerTrip
        timestamp StartDate
        timestamp EndDate
    }
    
    Transaction {
        int TransactionID PK
        int UserID FK
        float Amount
        varchar TransactionType
        timestamp TransactionDate
        varchar Status
        varchar PaymentMethod
        varchar ReferenceID
    }
    
    PaymentBooking {
        int PaymentID PK
        int TripID FK
        int UserID FK
        int CycleID FK
        float Amount
        int TransactionID FK
    }
    
    User ||--o{ UserBehavior : has
    User ||--o{ UserStatus : has
    User ||--o{ IncidentReport : reports
    User ||--o{ ResponseTeam : leads
    User ||--o{ CycleStation : owns
    User ||--o{ ReviewRating : rates
    User ||--o{ Booking : books
    User ||--o{ Trip : takes
    User ||--o{ Chat : participates
    User ||--o{ Transaction : makes
    User ||--o{ PaymentBooking : pays

    Cycle ||--o{ IncidentReport : involved_in
    Cycle ||--o{ TripCycles : included_in
    Cycle ||--o{ PaymentBooking : included_in
    Cycle ||--o{ CycleType : is_a

    CycleStation ||--o{ Cycle : has
    CycleStation ||--o{ Booking : has
    CycleStation ||--o{ Trip : start_from

    Trip ||--o{ TripCycles : has
    Trip ||--o{ Chat : discussed
    Trip ||--o{ PaymentBooking : included_in
    Trip ||--o{ UserStatus : belongs_to

    Booking ||--o{ PaymentBooking : paid_for
    Booking ||--o{ ReviewRating : referenced_in

    ResponseTeam ||--o{ IncidentReport : resolves
    
    RentalCharge ||--o{ CycleType : applies_to

    Subscription ||--o{ Transaction : involves
