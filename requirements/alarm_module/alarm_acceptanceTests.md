# Time Set
1.  GIVEN:  Power is on
            User has set time
    WHEN:   no user action is taken
    THEN:   time is tracked and correctly revolves from user's set time
            time is correctly displayed according to internal time tracking


2.  GIVEN:  Power is on
            toggle_set button has been pressed an even amout of times in the past 9 seconds
    WHEN:   User Presses the toggle_set button
    THEN:   MODE is toggled to TIME_SET
            clock display flashes
            clock displays last saved time
            

3.  GIVEN:  Power is on 
            toggle_set button has been pressed an odd number of times in the past 9 seconds
    WHEN:   User Presses the toggle_set button
    THEN:   MODE is toggled to ALARM_SET
            clock display flashes
            clock displays last saved alarm time


4.  GIVEN:  Power is on
            MODE is toggled to ALARM_SET or TIME_SET    
    WHEN:   User does not press set_hour, set_minute or toggle_set buttons for 10 seconds
    THEN:   clock display stops if it was previously flashing
            clock displays last saved clock time

5.  GIVEN:  Power is on
    WHEN:   User holds toggle_set button for 2 seconds
    THEN:   clock saves set alarm time and clock time
            clock display stops flashing if it was previously flashing
            clock displays last saved clock time

#TODO: MODE setup to where each mode makes something written on the 2nd line, ex. if alarm is set, should display "ARMED", if not, should display "PASSIVE"
            