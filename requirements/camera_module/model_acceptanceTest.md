1.  GIVEN:  Alarm signal is on
    WHEN:   All of the user's body is visible
    THEN:   The user's head coordinates are prioritized (forehead)

2.  GIVEN:  Alarm signal is on
    WHEN:   The user's head is not visible, but the rest of the body is visible
    THEN:   The user's leg coordinates are prioritized

3.  GIVEN:  Alarm signal is on
    WHEN:   The user's head and legs are not visible, but the rest of the body is visible
    THEN:   The user's torso coordinates are prioritized

4.  GIVEN:  Alarm signal is on
    WHEN:   Only one part of the user's body is visible
    THEN:   The visible part's coordinates are prioritized

5.  GIVEN:  Alarm signal is on
            The user is not detected
    WHEN:   The user is hiding under a blanket
    THEN:   The coordinate at the middle of the blanket is prioritized
