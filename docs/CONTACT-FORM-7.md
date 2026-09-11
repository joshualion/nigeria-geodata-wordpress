# Contact Form 7 Integration

Nigeria GeoData includes native Contact Form 7 fields.

Do **not** paste the normal `[nigeria_geodata ...]` shortcode into the Contact Form 7 form editor. Contact Form 7 uses its own form-tag system.

## State → LGA → Ward → Polling Unit

Paste into **Contact → Contact Forms → Form**:

```text
<label>State
[ngd_state* state]
</label>

<label>LGA / Area Council
[ngd_lga* lga depends:state]
</label>

<label>Ward
[ngd_ward* ward depends:lga]
</label>

<label>Polling Unit
[ngd_polling_unit* polling_unit depends:ward]
</label>

[submit "Submit"]
```

Then use these mail tags in the Contact Form 7 **Mail** tab:

```text
State: [state]
LGA: [lga]
Ward: [ward]
Polling Unit: [polling_unit]
```

## Electoral example

```text
[ngd_state* state]
[ngd_senatorial_district senate depends:state]
[ngd_federal_constituency federal depends:senate]
[ngd_lga lga depends:federal]
[ngd_ward ward depends:lga]
[ngd_polling_unit polling_unit depends:ward]
```

## Data source

These fields query the locally provisioned Nigeria GeoData database. Normal form selection does not call CampaignManager.ng.
