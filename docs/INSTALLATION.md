# Installation

## Requirements

- WordPress 6.3 or later
- PHP 7.4 or later
- HTTPS recommended for production sites
- outbound HTTPS access during provisioning

## Install from GitHub Releases

1. Open the public Nigeria GeoData repository.
2. Go to **Releases**.
3. Download the specifically named plugin package:

   ```text
   nigeria-geodata-x.y.z.zip
   ```

4. Upload that ZIP **directly** in WordPress Admin:

   ```text
   Plugins → Add New → Upload Plugin
   ```

5. Click **Install Now**.
6. Activate **Nigeria GeoData**.
7. Open **Nigeria GeoData** from the WordPress admin menu.

A correct Nigeria GeoData release ZIP is directly installable and contains one top-level plugin folder:

```text
nigeria-geodata-x.y.z.zip
└── nigeria-geodata/
    ├── nigeria-geodata.php
    ├── readme.txt
    ├── includes/
    └── assets/
```

You should **not** need to extract and re-zip the package yourself.

> Do not install GitHub's automatically generated **Source code (zip)** archive. Use the specifically named `nigeria-geodata-x.y.z.zip` release asset attached to the release.

### If WordPress says “No valid plugins were found”

Inspect the ZIP before trying to install it. If it contains another ZIP or a duplicated wrapper such as:

```text
nigeria-geodata/
└── nigeria-geodata/
    └── nigeria-geodata.php
```

then it is not the correctly packaged release asset. Download the specifically named release asset again rather than manually rebuilding the plugin package.

## Updating manually

1. Download the newer versioned ZIP from GitHub Releases.
2. Go to **Plugins → Add New → Upload Plugin**.
3. Upload the newer ZIP directly.
4. When WordPress detects the installed plugin, choose **Replace current with uploaded**.

Provisioned geography, coverage history and GeoForm submissions are stored in the WordPress database and are preserved during a normal plugin-file replacement.

## First use

1. Open **Nigeria GeoData → Dashboard**.
2. Purchase or enter a valid provisioning key.
3. Provision the authorised geography.
4. Verify the local data using **Data Explorer**.
5. Use selectors, APIs, Contact Form 7 integration or GeoForms.
