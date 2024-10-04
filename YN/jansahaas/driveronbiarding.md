sequenceDiagram
    participant Driver
    participant Kiosk as  Jan Sahas (   Kiosk at GAIL)
    participant Portal as Ayushman Bharat  Insurance Portal
    participant GAIL
    participant NammaYatri as Namma Yatri
    participant Hospitals
    participant Helpline as Emergency Helpline (Jan Sahas)


NammaYatri->>Driver: Display Ayushman Reg Banner Info with MAP
    Driver->>Kiosk: Arrives at Kiosk
    Kiosk->>Driver: Assists with Registration (Aadhaar, License)
    Kiosk->>Portal: Submits Driver Details
    Portal-->>Kiosk: Registration Confirmed
    Kiosk->>Driver: Provides Confirmation & Ayushman Bharat Card
    Driver->>GAIL: Reports enrollment success (monthly)
    Kiosk->>GAIL: Monthly Report of Registered Drivers
    Kiosk->>NammaYatri: Monthly Report to Namma Yatri

    Note over Driver, Hospitals: Emergency Scenario (Driver needs care)
    NammaYatri->>Driver: Display Ayushman Reg   Info with Hospitals

    Driver->>Helpline: Calls Emergency Helpline
    Helpline->>Hospitals: Verifies Driver's Eligibility with Ayushman Bharat
    Hospitals-->>Helpline: Confirms Cashless Treatment
    Helpline->>Driver: Guides Driver to Nearest Hospital

    Hospitals->>Driver: Provides Treatment
