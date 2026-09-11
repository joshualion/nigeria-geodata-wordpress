# Developer API

Nigeria GeoData exposes local REST, PHP and JavaScript APIs after provisioning.

All examples below query the local WordPress database.

## REST API

Base namespace:

```text
/wp-json/nigeria-geodata/v1/
```

### States / FCT

```http
GET /wp-json/nigeria-geodata/v1/entities?type=state
```

### LGAs in a State

```http
GET /wp-json/nigeria-geodata/v1/entities?type=lga&context=state:9
```

### Wards in an LGA

```http
GET /wp-json/nigeria-geodata/v1/entities?type=ward&context=lga:9:9
```

### Schema

```http
GET /wp-json/nigeria-geodata/v1/schema
```

### Status

```http
GET /wp-json/nigeria-geodata/v1/status
```

Supported query parameters include `type`, `context`, `search`, `page` and `per_page`.

## PHP helpers

```php
$states = nigeria_geodata_entities('state');
$lgas   = nigeria_geodata_entities('lga', 'state:9');
$entity = nigeria_geodata_entity('state:9');
$status = nigeria_geodata_status();
```

## JavaScript

```js
NigeriaGeoData.query('state').then(function (result) {
    console.log(result.items);
});
```

Context-aware query:

```js
NigeriaGeoData.query('lga', 'state:9').then(function (result) {
    console.log(result.items);
});
```

## Shortcode

Administrative selector:

```text
[nigeria_geodata fields="state,lga,ward,polling_unit"]
```

Electoral selector:

```text
[nigeria_geodata fields="state,senatorial_district,federal_constituency,lga,ward,polling_unit"]
```

Common options:

```text
labels="yes|no"
required="yes|no"
auto_select="yes|no"
value="external_id|name|code"
name_prefix="location"
```

## JavaScript events

Selector containers emit:

- `nigeria-geodata:ready`
- `nigeria-geodata:loaded`
- `nigeria-geodata:change`

These can be used by themes and plugins to react to geography selections.
