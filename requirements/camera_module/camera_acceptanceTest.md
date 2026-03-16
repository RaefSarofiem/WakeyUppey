1.  GIVEN:  Alarm signal is on
            Power is on
    WHEN:   The user is nearly motionless
    THEN:   The user is sprayed

2.  GIVEN:  Alarm signal is on
            Power is on
    WHEN:   The user is moving
    THEN:   The user is not sprayed

3.  GIVEN:  Alarm signal is on
            Power is on
    WHEN:   The user is lying down
    THEN:   The user is sprayed

4.  GIVEN:  Alarm signal is off
            Power is on
    WHEN:   The user is visible to the camera
    THEN:   No action is taken and the user is not sprayed
