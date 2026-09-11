# Changelog

All notable public changes to Nigeria GeoData are documented here.

## [1.0.0] - 2026-09-11

### Added

- National, State/FCT, Senatorial District, Federal Constituency and LGA/Area Council provisioning scopes
- one-time `NGWP-...` provisioning keys
- automatic payment-confirmed key issuance through CampaignManager.ng
- resumable batched provisioning with persistent checkpoints
- additive coverage for multiple authorised scopes on one WordPress site
- National coverage completion handling
- local storage for geopolitical zones, States/FCT, Senatorial Districts, Federal Constituencies, LGAs, Wards and Polling Units
- relationship-aware local query engine
- cascading `[nigeria_geodata]` selectors
- Data Explorer
- Coverage & Expansion administration
- local REST API
- public PHP helper API
- JavaScript query API and events
- native Contact Form 7 geography fields
- built-in GeoForms form builder
- local GeoForms submission storage
- CSV submission export
- administrator notification emails
- optional submitter confirmation emails
- Plugin Check compliance fixes
- CI validation across PHP 7.4, 8.1 and 8.3

### Notes

- Provisioning is delivered through CampaignManager.ng.
- Normal geography queries run from the local WordPress database after provisioning.
- Native adapters for additional form builders are planned for future versions after compatibility testing.
