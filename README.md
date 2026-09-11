# Nigeria GeoData

**Nigerian Administrative & Electoral Geography for WordPress**

Nigeria GeoData is a WordPress plugin by **Govware** for provisioning and using Nigerian administrative and electoral geography directly inside WordPress.

<p>
  <a href="https://github.com/joshualion/nigeria-geodata-wordpress/releases/latest"><img src="https://img.shields.io/github/v/release/joshualion/nigeria-geodata-wordpress?label=Latest%20Release&style=for-the-badge&color=008F5A" alt="Latest Release"></a>
  <a href="https://github.com/joshualion/nigeria-geodata-wordpress/releases"><img src="https://img.shields.io/github/downloads/joshualion/nigeria-geodata-wordpress/total?label=Total%20Downloads&style=for-the-badge&color=0A7F55" alt="Total Downloads"></a>
  <img src="https://img.shields.io/badge/Public%20Since-11%20Sep%202026-006B45?style=for-the-badge" alt="Public Since">
  <img src="https://img.shields.io/badge/Release%20Channel-Stable-008F5A?style=for-the-badge" alt="Release Channel">
</p>

<p>
  <a href="https://github.com/joshualion/nigeria-geodata-wordpress/releases/latest"><img src="https://img.shields.io/github/release-date/joshualion/nigeria-geodata-wordpress?display_date=published_at&label=Latest%20Update&style=for-the-badge&color=008F5A" alt="Latest Update"></a>
  <a href="https://github.com/joshualion/nigeria-geodata-wordpress/releases/latest/download/nigeria-geodata-1.0.0.zip"><img src="https://img.shields.io/badge/Download-WordPress%20Plugin-008F5A?style=for-the-badge&logo=wordpress&logoColor=white" alt="Download Plugin"></a>
  <a href="docs/INSTALLATION.md"><img src="https://img.shields.io/badge/Installation-Guide-0A7F55?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Installation Guide"></a>
  <a href="https://campaignmanager.ng/nigeria-geodata/wordpress"><img src="https://img.shields.io/badge/Provisioning-Service-Visit-006B45?style=for-the-badge" alt="Provisioning Service"></a>
</p>

---

## What Nigeria GeoData does

Nigeria GeoData gives WordPress developers a structured local geography layer for Nigerian administrative and electoral data.

It is designed for campaign websites, civic-tech systems, constituency portals, membership platforms, field operations, research projects, public-sector applications and other WordPress projects that need dependable Nigerian geography selectors and relationships.

The plugin can provision and locally store:

- **Nigeria**
- **6 Geopolitical Zones**
- **37 States / FCT**
- **109 Senatorial Districts**
- **360 Federal Constituencies**
- **774 LGAs / Area Councils**
- **8,809 Wards / Registration Areas**
- **176,846 Polling Units**

These are the current Nigeria GeoData dataset totals exposed by the provisioning service.

## Why Nigeria GeoData?

Many WordPress projects need more than a simple list of Nigerian States and LGAs. Nigeria GeoData is built for applications that need deeper geographic relationships such as:

```text
Nigeria
→ Geopolitical Zone
→ State / FCT
→ LGA / Area Council
→ Ward / Registration Area
→ Polling Unit
```

Electoral relationships also include:

```text
State
→ Senatorial District
→ Federal Constituency
```

Once a purchased scope is successfully provisioned, normal geography queries are served from the site's **local WordPress database**.

## Feature overview

- **National, State/FCT, Senatorial District, Federal Constituency and LGA/Area Council provisioning scopes**
- **One-time `NGWP-...` provisioning keys** tied to the authorised site/scope
- **Automatic payment-confirmed key issuance** through CampaignManager.ng
- **Resumable batched provisioning** with persistent checkpoints
- **Additive coverage** for installations that expand over time
- **Local relationship-aware query engine**
- **Cascading WordPress selectors** with optional/skippable levels
- **Data Explorer** for browsing local geography
- **Coverage & Expansion** administration
- **Read-only local REST API**
- **Public PHP helper API**
- **JavaScript query API and events**
- **Native Contact Form 7 integration**
- **Built-in GeoForms form builder**
- **Local form submissions, email notifications and CSV export**
- **Theme-friendly semantic HTML controls**

## Coverage scopes

Nigeria GeoData supports geography provisioning for:

- **National**
- **State / FCT**
- **Senatorial District**
- **Federal Constituency**
- **LGA / Area Council**

Pricing is displayed in USD while payment is processed through the supported CampaignManager.ng payment flow in Nigerian Naira where applicable.

A provisioning key is one-time-use for its own authorised coverage. The WordPress installation itself is not limited to one purchase.

### Additive coverage

A site may add geography incrementally:

```text
Calabar South LGA
+ Calabar Municipality LGA
= both LGAs available locally
```

Later:

```text
Several LGAs
+ Cross River State
= overlaps reused + remaining State geography added
```

And later:

```text
Cross River State
+ National
= existing Cross River records reused + remaining Nigerian geography added
```

Successful coverage is not deleted simply because another package is provisioned.

Once complete **National** coverage exists, the plugin treats the installation as geographically complete and no longer prompts for additional coverage.

## Quick installation

1. Go to **[GitHub Releases](https://github.com/joshualion/nigeria-geodata-wordpress/releases/latest)**.
2. Download the specifically named plugin file:

   ```text
   nigeria-geodata-1.0.0.zip
   ```

3. In WordPress Admin go to:

   ```text
   Plugins → Add New → Upload Plugin
   ```

4. Upload the ZIP and activate **Nigeria GeoData**.
5. Open **Nigeria GeoData** from the WordPress admin menu.
6. Purchase or enter a valid provisioning key.
7. Provision the geography.
8. Verify the local data using **Data Explorer**.

> **Important:** do not install GitHub's automatically generated “Source code (zip)” archive. Download the specifically named `nigeria-geodata-x.y.z.zip` release asset.

See the full **[Installation Guide](docs/INSTALLATION.md)**.

## Purchase & provisioning

Paid geography provisioning is delivered through **CampaignManager.ng**.

- Provisioning service: https://campaignmanager.ng/nigeria-geodata/wordpress
- External Service & Privacy Disclosure: https://campaignmanager.ng/legal/nigeria-geodata-wordpress-service-disclosure
- Campaign Manager legal agreement: https://campaignmanager.ng/legal/campaign-manager-agreement
- Campaign Manager: https://campaignmanager.ng/

After successful payment confirmation, the service issues a site-bound `NGWP-...` provisioning key automatically.

Provisioning is resumable. If a browser refresh, network interruption or long-running import pauses the process, the plugin stores its last successful checkpoint and can continue instead of starting the entire dataset again.

See **[Purchase & Provisioning](docs/PROVISIONING.md)**.

## Cascading selectors

Basic administrative path:

```text
[nigeria_geodata fields="state,lga,ward,polling_unit"]
```

With electoral levels:

```text
[nigeria_geodata fields="state,senatorial_district,federal_constituency,lga,ward,polling_unit"]
```

Levels may be omitted where the local relationship graph can resolve the requested next level.

## Built-in GeoForms

Nigeria GeoData includes its own focused form builder, so many projects do not need another form plugin.

Create forms under:

```text
Nigeria GeoData → Forms
```

Then publish them with a generated shortcode such as:

```text
[nigeria_geodata_form id="1"]
```

GeoForms supports:

- Text
- Email
- Phone
- Textarea
- Select
- Checkbox
- Nigeria GeoData selector
- local submission storage
- administrator notification emails
- optional submitter confirmation emails
- CSV export

See **[GeoForms](docs/GEOFORMS.md)**.

## Contact Form 7

Nigeria GeoData registers native Contact Form 7 form-tags:

```text
[ngd_state* state]
[ngd_lga* lga depends:state]
[ngd_ward* ward depends:lga]
[ngd_polling_unit* polling_unit depends:ward]
```

Mail tags can then use:

```text
[state]
[lga]
[ward]
[polling_unit]
```

See **[Contact Form 7 Integration](docs/CONTACT-FORM-7.md)**.

## Developer APIs

### REST

```text
GET /wp-json/nigeria-geodata/v1/entities?type=state
GET /wp-json/nigeria-geodata/v1/entities?type=lga&context=state:9
GET /wp-json/nigeria-geodata/v1/entities?type=ward&context=lga:9:9
GET /wp-json/nigeria-geodata/v1/schema
GET /wp-json/nigeria-geodata/v1/status
```

### PHP

```php
$states = nigeria_geodata_entities('state');
$lgas   = nigeria_geodata_entities('lga', 'state:9');
$status = nigeria_geodata_status();
```

### JavaScript

```js
NigeriaGeoData.query('lga', 'state:9').then(function (result) {
    console.log(result.items);
});
```

See **[Developer API](docs/DEVELOPER-API.md)**.

## Theme compatibility

Frontend output uses normal semantic HTML controls and lightweight plugin-specific CSS. Themes and custom CSS can override colours, typography, spacing, borders, buttons and layout without modifying plugin core files.

## Documentation

- [Documentation index](docs/README.md)
- [Installation Guide](docs/INSTALLATION.md)
- [Purchase & Provisioning](docs/PROVISIONING.md)
- [Developer API](docs/DEVELOPER-API.md)
- [Contact Form 7 Integration](docs/CONTACT-FORM-7.md)
- [GeoForms](docs/GEOFORMS.md)
- [FAQ](docs/FAQ.md)
- [Screenshot Guide](docs/SCREENSHOTS.md)
- [Changelog](CHANGELOG.md)

## Updates

Stable versions are published through **[GitHub Releases](https://github.com/joshualion/nigeria-geodata-wordpress/releases)**.

This repository is the official **public documentation and release-distribution home** for Nigeria GeoData. Active plugin development, tests and unreleased source history are maintained separately by Govware.

For each stable release, download the versioned asset:

```text
v1.0.0
└── nigeria-geodata-1.0.0.zip
```

Future releases will follow semantic versioning where practical, for example `v1.0.1`, `v1.1.0`, and `v2.0.0`.

## Community and contributions

Useful public contributions are welcome for documentation, tutorials, installation guidance, screenshots, translations, reproducible bug reports and feature ideas.

The active plugin development source tree is not maintained in this public release repository, so application-level code changes are assessed by the maintainers rather than accepted here as direct source-code pull requests.

See **[CONTRIBUTING.md](CONTRIBUTING.md)**.

## Security

Please do **not** publish passwords, provisioning keys, session tokens, site credentials or personal data in public issues.

Read **[SECURITY.md](SECURITY.md)** for responsible reporting guidance.

## External service & privacy

CampaignManager.ng supplies the paid geography provisioning service.

During provisioning, Nigeria GeoData sends the provisioning key, WordPress site URL, installation identifier, plugin version and provisioning-session information required to deliver the authorised dataset.

After provisioning, normal geography queries use the local WordPress database. GeoForms and Contact Form 7 submission contents are not sent to CampaignManager.ng by the geography query layer.

Read the dedicated **[External Service & Privacy Disclosure](https://campaignmanager.ng/legal/nigeria-geodata-wordpress-service-disclosure)** for details about service operation, transmitted data, payment handling, retention and local-versus-remote processing.

## Licence

Nigeria GeoData is distributed under **GPL-2.0-or-later**.

See **[LICENSE](LICENSE)**.

---

<div align="center">

**Nigeria GeoData**  
Nigerian Geography for WordPress  
Developed by **Govware**  
[CampaignManager.ng](https://campaignmanager.ng/nigeria-geodata/wordpress)

</div>
