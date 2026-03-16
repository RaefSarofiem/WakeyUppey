GIVEN: alarm signal is on
WHEN: all of user's body is visible
THEN: User's head coordinates are prioritized (forhead)

GIVEN: alarm signal is on
WHEN: User's head is not visible, but rest of body is
THEN: User's leg coordinates are prioritized

GIVEN: alarm signal is on
WHEN: user's head and legs are not visible, but rest of body is
THEN: User's torso coordinates are prioritized

GIVEN: alarm signal is on
WHEN: only one part of User's body is visible
THEN: visible part's coordinates are prioritized

GIVEN: alarm signal is on, user is not detected
WHEN: Hiding under blanket
THEN: prioritize coordinate to middle of blanket.