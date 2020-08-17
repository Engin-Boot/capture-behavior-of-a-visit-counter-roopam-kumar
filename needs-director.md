# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given counter which counts each patient visit without error
  When I click on counter at any time of day
  Then I get the number of patients visited till that point in time

Scenario: Compute parking slots to reserve for visiting specialists

  Given a system which tells the number of parking slots empty at the current moment
  When the number of empty parking slots is lesser than the number of visiting specialists
  Then I get an alert so as to provide a parking slot
