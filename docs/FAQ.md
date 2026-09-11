# FAQ

## Is Nigeria GeoData free?

The WordPress plugin code is GPL-licensed. Geography provisioning is a paid external service delivered through CampaignManager.ng.

## Does the plugin query CampaignManager.ng every time a visitor opens a form?

No. After successful provisioning, normal selector, Data Explorer, REST, PHP, JavaScript, GeoForms and Contact Form 7 geography queries use the local WordPress database.

## Can I start with one LGA and add another later?

Yes. Coverage is additive. You can provision another authorised LGA, constituency, State or National package later without deleting successful existing coverage.

## Can I upgrade from State coverage to National?

Yes. Existing overlapping records are reused and the remaining authorised National geography is added.

## What happens after National coverage is complete?

National is the terminal geography scope. The plugin no longer prompts for another geography purchase on that installation.

## Can provisioning resume after an interruption?

Yes. Provisioning is batched and checkpoints are stored locally. A paused process can resume from the last successful checkpoint when the authorised session/key remains valid.

## Does it support Contact Form 7?

Yes. Nigeria GeoData includes native Contact Form 7 form-tags.

## Does it support WPForms, Gravity Forms, Fluent Forms or Elementor Forms?

The local REST, PHP, JavaScript and shortcode interfaces can be used by developers today. Dedicated native adapters are planned only after compatibility testing with those plugins.

## Does Nigeria GeoData have its own form builder?

Yes. GeoForms can create application, registration and data-collection forms using ordinary fields plus cascading Nigeria GeoData selectors.

## Where are GeoForm submissions stored?

They are stored locally in WordPress and can be reviewed or exported as CSV from the Nigeria GeoData administration area.

## Which ZIP should I install from GitHub?

Use the explicitly named release asset such as:

```text
nigeria-geodata-1.0.0.zip
```

Do not use GitHub's automatically generated “Source code (zip)” archive.
