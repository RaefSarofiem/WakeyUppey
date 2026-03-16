1.  GIVEN:  Power is connected and sufficient
            The tracking system is running
    WHEN:   A move command is received
    THEN:   The nozzle is moved to the correct position so the stream of water lands within a 5 cm radius of the commanded coordinate
            The nozzle reaches that position within 1/4 of a second of receiving the command
