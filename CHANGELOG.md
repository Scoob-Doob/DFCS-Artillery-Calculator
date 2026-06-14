# Changelog

## v0.1.3 - 14/06/26

### Added

- Added DFCS Ammunition controls with projectile and charge quantity entry.
- Added ammunition inventory display to FDC Unit Data with expandable unit rows.
- Added ammunition and charge capability checks to mission sending and ballistic solutions.
- Added DFCS ammunition deduction when Rounds Complete is sent.
- Added FDC warning flow for units that cannot meet ammunition or charge requirements.
- Added HE PD and HE VT method of engagement options, both using HE M107 projectile data with separate fuze display.
- Added Do Not Load command support, displaying DNL in DFCS ammunition data and blocking DFCS Ready.
- Added Mission Status Monitor command buttons for Ping, Resend, and End of Mission.
- Added target detail dropdowns for target lists and stored targets, including adjustments, BDA, and final target grid.
- Added adjustment history with recorded corrections and running totals.
- Added target number and target grid autofill from saved targets.
- Added altitude UP/DOWN corrections in the Adjustment tab.
- Added azimuth of lay and arc of fire data for M777 units.

### Fixed

- Fixed M777 ballistic data to use the updated 1.7 table source.
- Fixed M777 altitude correction direction for low-angle and high-angle solutions.
- Fixed M777 charge display to use 1L, 2L, 3H, 4H, and 5H.
- Fixed high-angle and low-angle warning logic for forced charge and angle selections.
- Fixed range rings to follow the updated M777 firing table data.
- Fixed DFCS End of Mission acknowledgement wiping newer mission data.
- Fixed MSM End of Mission not reliably sending EOM to DFCS users.
- Fixed resend behavior for denied missions and removed the notification sound loop.
- Fixed mission calculation preserving user-edited mission fields after opening a saved target.
- Fixed DFCS Ready being available while DNL is active.
- Fixed TOT countdown behavior to use set Z time minus time of flight.
- Fixed adjustment corrections so direction records are retained and applied.
- Fixed adjustment direction input to cap at four digits and auto-pad short entries.
- Fixed Ammo Capable display to use plain Y/N text.

### Changed

- Reorganized the FDC ballistic solution table to follow CPO sequence of orders.
- Changed ballistic solution ammunition display so HE PD and HE VT show as HE M107, with PD/VT shown in the Fuze column.
- Changed VT fuze setting display to only appear for VT fuzes and use time of flight minus 0.1 seconds.
- Changed DFCS solution layout to separate Bearing, Ammunition, Fuze Setting, Elevation, Method of Fire Control, and AOF.
- Changed DFCS ammunition display to include round count and charge increment.
- Changed DFCS Fuze Setting display so VT fuzes include the calculated fuze time setting.
- Changed method of fire control display to show WR, AMC, TOT, or DNL separately from FFE/Adjust Fire.
- Changed unit naming from A1/B1/C1/D1 to 1A/1B/1C/1D across FDC and DFCS displays.
- Changed FDC weapon selection name from M777 to M777 (PandaMod).
- Changed DFCS Moving/Stationary menu layout into Location Update, Arc of Fire, and Crest Data sections.
- Changed DFCS and FDC mobile layouts for better phone scaling. (WIP)
- Changed FDC mobile sidebar behavior so the toggle moves with the sidebar.
- Changed DFCS ammunition table styling and removed number spinner arrows.
- Changed notification sounds for DFCS End of Mission and FDC Deny to play slower.
- Disabled calculator wind effects while retaining the met data UI and firing-table wind data.


## v0.1.2 - 09/06/2026

### Added

- Updated M777 Firing tables for 1.7 Update
- Updated M252 Firing tables for 1.7 Update
- Added expanded M252 ballistic data for M821 HE, M853A1 illumination, M819 smoke, and M879 practice rounds

### Fixed

- Fixed low angle calculation relating to Delta elevation

### Changed

- Disabled Met Data entry in settings


## v0.1.1 - 26/05/2026

### Fixed

- Fixed DFCS location input not always updating when switching between Moving, Apply, and Stationary.
- Fixed check firing being enforced while missions could still be sent to DFCS users, causing uncontrollable mission receive prompts.
- Fixed denied targets showing as current in the Mission Status Monitor.

### Added

- Added updated M777 range tables, including high- and low-angle fire.
- Added browser cache bypass for ballistic JSON fetches, so edits load properly.
- Added minimum and maximum elevation limits on mortar solutions.
- Added recorded targets to Map View with assigned target numbers.
- Added a Geometries tab with No Fire Area functions.
- Added a grid readout on Map View.
- Added DFCS local crest input.
- Added mission number to the Mission Status Monitor for simultaneous-mission tracking.
- Added Map View controls.
- Added available-unit display on Map View for stationary units.
- Added dynamic Map View grid scaling between 10km, 1km, and 100m grid spacing based on zoom.
- Added a Map View scale label showing the current grid square size.
- Added a right-click Map View target action to center the target on screen.
- Added right-click Map View unit actions to center units on screen and toggle range rings.
- Added Map View target hover labels.
- Added No Fire Area target blocking, so firing solutions fail when the target is inside an NFA.
- Added a Local Crest result column with Y/N status and N/A elevation when blocked.
- Added Map View range rings for available and active units based on the current weapon system.

### Changed

- Allowed the calculator to pick the best shell and charge solution based on the smallest PEr instead of only minimum time of flight.
- Updated target creation inputs to better match the grid mission page.
- Updated M777 firing table data to better match the mod.
- Geometries can now be built for situational awareness and controlling fires.
- Map View now supports zooming and click-drag navigation.
- Mission Status Monitor now displays the target number next to units in mission to help deconflict simultaneous missions and current engagements.
- Changed DFCS Ready Sent selected colour to match Rounds Complete Sent.
- Changed the Crest button to CREST DATA and moved it next to Ping.
- Changed Plan View naming and styling to Map View.
- Removed estimated PEr display from firing solutions.


## v0.1.0 - 19/05/2026

- Initial tracked version.

- Added changelog.
- Added meteorological data input.
- Added volume slider under the Settings tab.
- Added target lists.
- Added Fire Plan tab with schedule **WIP**.
- Added Emergency Check Firing button.
- Added Zulu clock to the DFCS user screen.
- Added Clear Data button to the FDC fire mission screen.

- Fixed Adjustment tab issue.
- Fixed issue with data being left on screen after EOM is given.
- Fixed DFCS ping function so it only returns success on FDC acknowledgement.

- Removed range from DFCS.
- Removed notifications for sound effects.

- New missions retain user input when switching tabs.
- QoL improvements for UI and spacing.
- Target number autofills saved target data.
- Targets in target lists can be opened to initiate a fire mission.
- Changed Unit Location button to Unit Setup.
- Inputting 6- or 8-figure grids autofills them to 10 figures.
- Ammunition selection now affects the DFCS screen instead of displaying 'HE'.
