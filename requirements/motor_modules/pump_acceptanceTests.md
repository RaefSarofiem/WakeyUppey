## power
1.  GIVEN:  Power is connected and sufficient
    WHEN:   Signal is being sent to turn on pump
    THEN:   Pump motor turns on

2.  GIVEN:  Power is connected and sufficient
    WHEN:   Signal is not being sent to turn on pump
    THEN:   Pump motor turns off
# what happens when power is insufficient? is there a way to detect that and send a notification to the alarm?