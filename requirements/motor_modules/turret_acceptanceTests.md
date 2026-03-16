1.  GIVEN:  Power is connected and sufficent
            Tracking system is running
    WHEN:   move command is recieved
    THEN:   the nozzle is moved to the correct position that allows the stream of water coming from the nozzle to land within 5 cm radius of the commanded coordinate
            the nozzle must reach the position within 1/4 of a second of recieving the command