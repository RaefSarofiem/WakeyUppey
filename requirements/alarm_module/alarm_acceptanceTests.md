# Alarm Acceptance Tests

1.  GIVEN:  Power is on
            The user has set time
    WHEN:   No user action is taken
    THEN:   Time is tracked correctly from the user's set time
            Time is displayed according to the internally tracked time


2.  GIVEN:  Power is on
            The `toggle_set` button has been pressed an even number of times in the past 9 seconds
    WHEN:   The user presses the `toggle_set` button
    THEN:   Mode is toggled to `TIME_SET`
            The display flashes
            The last saved time is displayed
            

3.  GIVEN:  Power is on 
            The `toggle_set` button has been pressed an odd number of times in the past 9 seconds
    WHEN:   The user presses the `toggle_set` button
    THEN:   Mode is toggled to `ALARM_SET`
            The display flashes
            The last saved alarm time is displayed


4.  GIVEN:  Power is on
            Mode is toggled to `ALARM_SET` or `TIME_SET`
    WHEN:   The user has not pressed `set_hour`, `set_minute`, or `toggle_set` for 10 seconds
    THEN:   The display stops flashing if it was previously flashing
            The last saved clock time is displayed
            

5.  GIVEN:  Power is on
    WHEN:   The user holds the `toggle_set` button for 2 seconds
    THEN:   The clock saves the set alarm time and clock time
            The display stops flashing if it was previously flashing
            The last saved clock time is displayed
            The alarm is activated
            The display shows "ARMED" below the time

6.  GIVEN:  Power is on
            The user has not pressed the `toggle_set` button for 10 seconds
    WHEN:   The user holds the `set_hour` button for 5 seconds
    THEN:   The alarm is deactivated
            The display shows "PASSIVE" below the time

7.  GIVEN:  Power is on
            The user has pressed `toggle_set`, `set_minute`, and/or `set_hour` in the last 9 seconds
            The current displayed hour is less than 11
    WHEN:   The user presses the `set_hour` button
    THEN:   One hour is added to the displayed time

8.  GIVEN:  Power is on
            The user has pressed `toggle_set`, `set_minute`, and/or `set_hour` in the last 9 seconds
            The current displayed minutes are less than 59
    WHEN:   The user presses the `set_minute` button
    THEN:   One minute is added to the displayed time

9.  GIVEN:  Power is on
            The user has pressed `toggle_set`, `set_minute`, and/or `set_hour` in the last 9 seconds
            The current displayed minutes are 59
            The current displayed hour is less than 11
    WHEN:   The user presses the `set_minute` button
    THEN:   One hour is added and 59 minutes are subtracted from the displayed time

10.  GIVEN:  Power is on
             The user has pressed `toggle_set`, `set_minute`, and/or `set_hour` in the last 9 seconds
             The current displayed minutes are 59
             The current displayed hour is 11
    WHEN:    The user presses the `set_minute` button
    THEN:    One hour is added and 59 minutes are subtracted from the displayed time
             The display toggles meridiem / post meridiem (`AM/PM`)
          

11.  GIVEN:  Power is on
             The user has pressed `toggle_set`, `set_minute`, and/or `set_hour` in the last 9 seconds
             The current displayed minutes are 59
             The current displayed hour is 12
    WHEN:    The user presses the `set_minute` button
    THEN:    Eleven hours and 59 minutes are subtracted from the displayed time

12.  GIVEN:  Power is on
             The user has pressed `toggle_set`, `set_minute`, and/or `set_hour` in the last 9 seconds
             The current displayed hour is 11
    WHEN:    The user presses the `set_hour` button
    THEN:    One hour is added to the displayed time
             The display toggles meridiem / post meridiem (`AM/PM`)

13.  GIVEN:  Power is on
             The user has pressed `toggle_set`, `set_minute`, and/or `set_hour` in the last 9 seconds
             The current displayed hour is 12
    WHEN:    The user presses the `set_hour` button
    THEN:    Eleven hours are removed from the displayed time


14. GIVEN:  Power is on
            Mode is toggled to `ALARM_SET` or `TIME_SET`
            The user has pressed `set_hour` or `set_minute` in the past 9 seconds
    WHEN:   The user holds the `set_minute` button
    THEN:   The displayed time increases in accelerating half-second steps while the button remains held
            The minutes added per half-second increase exponentially from the initial increment
            The minutes added per half-second are capped at 8 minutes
            Releasing the button stops further minute changes immediately

15.  GIVEN:  Power is on
             The user has set time
             The current displayed minutes are less than 59
    WHEN:    One minute passes with no user input
    THEN:    The displayed minutes increase by 1
             The displayed hour remains unchanged
             The displayed meridiem / post meridiem (`AM/PM`) remains unchanged

16.  GIVEN:  Power is on
             The user has set time
             The current displayed time is X:59 AM, where X is 1 through 10
    WHEN:    One minute passes with no user input
    THEN:    The displayed time updates to X+1:00 AM

17.  GIVEN:  Power is on
             The user has set time
             The current displayed time is 11:59 AM
    WHEN:    One minute passes with no user input
    THEN:    The displayed time updates to 12:00 PM
             The display toggles meridiem / post meridiem (`AM/PM`)

18.  GIVEN:  Power is on
             The user has set time
             The current displayed time is 12:59 PM
    WHEN:    One minute passes with no user input
    THEN:    The displayed time updates to 1:00 PM
             The displayed meridiem / post meridiem (`AM/PM`) remains unchanged

19.  GIVEN:  Power is on
             The user has set time
             The current displayed time is 11:59 PM
    WHEN:    One minute passes with no user input
    THEN:    The displayed time updates to 12:00 AM
             The display toggles meridiem / post meridiem (`AM/PM`)

20.  GIVEN:  Power is on
             The user has set time
             The current displayed time is 12:59 AM
    WHEN:    One minute passes with no user input
    THEN:    The displayed time updates to 1:00 AM
             The displayed meridiem / post meridiem (`AM/PM`) remains unchanged

21.  GIVEN:  Power is on
             The alarm is armed
             The current water amount is below the X threshold
    WHEN:    The user presses any button or no button is pressed
    THEN:    The display shows "LOW WATER"
             "LOW WATER" remains displayed while the alarm is armed and the water amount remains below the X threshold

22.  GIVEN:  Power is on
             The current battery power is below the X threshold
    WHEN:    The user presses any button or no button is pressed
    THEN:    The display shows "LOW BATTERY"
             "LOW BATTERY" remains displayed while the battery power remains below the X threshold