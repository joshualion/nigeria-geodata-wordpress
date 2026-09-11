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

4. In WordPress Admin go to:

   ```text
   Plugins → Add New → Upload Plugin
   ```

5. Select the ZIP and click **Install Now**.
6. Activate **Nigeria GeoData**.
7. Open **Nigeria GeoData** from the WordPress admin menu.

> Do not install GitHub's automatically generated “Source code (zip)” archive. Use the versioned Nigeria GeoData release asset.

## Updating manually

1. Download the newer versioned ZIP from GitHub Releases.
2. Go to **Plugins → Add New → Upload Plugin**.
3. Upload the newer ZIP.
4. When WordPress detects the installed plugin, choose **Replace current with uploaded**.

Provisioned geography, coverage history and GeoForm submissions are stored in the WordPress database and are preserved during a normal plugin-file replacement.

## First use

1. Open **Nigeria GeoData → Dashboard**.
2. Purchase or enter a valid provisioning key.
3. Provision the authorised geography.
4. Verify the local data using **Data Explorer**.
5. Use selectors, APIs, Contact Form 7 integration or GeoForms.
