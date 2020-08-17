# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given a server which preserves the last visit count
  When I restart the server
  Then the device updates the visit count

Scenario: Reconcile counts if the sensor is offline for a while

  Given the sensor records and stores the last count before going offline
  When the sensor comes online again
  Then the count refreshes to the latest value
