---
config:
  layout: elk
---
flowchart TB
    %% Vision Block
    V["Vision: Integrated, Digitized, Open Mobility Ecosystem in Karnataka"] 
    %% Core Components
    subgraph Components
        A1["Real-time Tracking"]
        A2["Metro Data Integration"]
        A3["Bus Data Integration"]
        A4["SubUrban Rail Schedules"]
        A5["Launch Booking Platform"]
        A6["Metro Booking"]
        A7["Booking of Autos & Cabs"]
        A8["ONDC Enabled Services"]
        A9["Bus Booking"]
        A10["SubUrban Rail Booking"]
        A11["Trip Stitching"]
        A12["BMTC/KSRTC Driver App"]
    end
    %% Pilot Version
    subgraph Pilot
        P[" Namma Yatri Pilot "]
        P --> A5
        P --> A6
        P --> A7
        P --> A8
        P --> A9
        P --> A10
        P --> A11
        P --> A12
    end
    %% Connections
    V --> Components
    Components --> Pilot
    A1 --> A5 & A6 & A7 & A8 & A9 & A10
    A2 --> A6
    A3 --> A9
    A4 --> A10
