flowchart TD
    %% Inputs Section
    subgraph Inputs
        A1["Funding"]
        A2["Land Allocation"]
        A3["Policy Support"]
        A4["EV Infrastructure"]
        A5["Driver Skilling Programs"]
        A6["EV Autos"]
        A7["Support from Nirbhaya Scheme"]
        A8["NAMMA YATRI Platform Integration"]
    end

    %% Outputs Section
    subgraph Outputs
        B1["Operational Charging Stations"]
        B2["Trained Women Auto Drivers"]
        B3["Deployed Electric Autos"]
        B4["Enhanced Public Transport Options"]
    end

    %% Process Block
    Process["Setup of Mahila Shakti Auto Program"]

    %% Impact Block
    subgraph Impact
        I1["Increased Women Employment"]
        I2["Safe Rides for Women"]
        I3["Reduced Emissions"]
        I4["Economic Empowerment of Women"]
        I5["Improved Urban Mobility"]
    end

    %% Connections
    Inputs --> Process
    Process --> Outputs
    Outputs --> Impact
