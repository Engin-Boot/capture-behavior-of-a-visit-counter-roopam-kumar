# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given a device which will record the visitor count without error
  When I accumulate and analyse the visitor count for the week of operation
  Then I will get the trend in the report

Scenario: Alert when seating capacity is full

  Given a device which will record seating capacity in real time
  When the seating capacity reaches its maximum limit
  Then an alert will be issued by the system
