
GIVEN: alarm signal is on
WHEN: User is nearly motionless
THEN: User is sprayed

GIVEN: alarm signal is on
WHEN: User is moving
THEN: User is not sprayed

GIVEN: alarm signal is on
WHEN: user is laying down
THEN: user is sprayed

GIVEN: alarm signal is off
WHEN: User is visible to camera
THEN: no action taken (user is not sprayed)
