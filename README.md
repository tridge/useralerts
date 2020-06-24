# User Alerts
## User Alerts for ArduPilot

A User Alert is a formal report of an ArduPilot issue that may affect the safe operation of a vehicle. An "issue" is typically a bug report or GitHub Issue. "Safe Operation" is the ability of a vehicle to reliably respond to user commands in a timely manner AND the ability of the vehicle to reliably follow commanded actions in automated flight modes.

Examples of Safe Operation issues include:
- Corrupted packets in I2C bus locking up the flight controller
- Non-commanded disarming whilst in-flight
- Malformed stored waypoint causes vehicle to fly away whilst in AUTO mode
- Triggering of the watchdog reset whilst in-flight

Examples of issues which are NOT Safe Operation issues include:
- Sub-optimal parameter values that lead to poor navigation performance
- User error or misunderstanding of parameter configuration
- Issues that, if experienced, an average user would be likely to safely recover from

User Alerts will only be for ArduPilot software issues. Manufacturer hardware will not be included at this stage, although this may be reviewed at a later date.

## The folders

The folders are organised as such:

 - alerts (All User Alerts)
 - examples (Examples of User Alerts file format. The "EX\*.json" are valid files, the "BAD\*.json" are not valid)
 - scripts (CI and publishing scripts)

## The file format

Each User Alert is contained in a single json file, in the "alerts" folder.

A template is available at ``template.json``

Field definitions are in the ArduPilot Wiki (add link)

## Process for releasing User Alerts

See ArduPilot Wiki (add link)

## Notes for querying data (GCS, etc)

Simply querying the site xxxxxx will return a json array of all user alerts.
These can then be filtered by the ``versionFrom``, ``versionFixed``,
``affectedFirmware`` and ``hardwareLimited`` fields to match with the
user's autopilot and display any relevant user alerts.

Querying the site yyyyy will return *example* user alerts for testing purposes.


