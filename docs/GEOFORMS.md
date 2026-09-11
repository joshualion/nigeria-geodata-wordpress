# GeoForms

GeoForms is Nigeria GeoData's built-in form builder.

It allows WordPress administrators to create forms that combine ordinary input fields with Nigerian geographic selectors without installing another form plugin.

## Create a form

Go to:

```text
Nigeria GeoData → Forms
```

Create and publish a form. The form receives a shortcode such as:

```text
[nigeria_geodata_form id="1"]
```

Place that shortcode on a page or post.

## Supported field types

- Text
- Email
- Phone
- Textarea
- Select
- Checkbox
- Nigeria GeoData selector

## Geographic fields

A GeoData field can include the required levels, for example:

```text
State
→ LGA
→ Ward
→ Polling Unit
```

or:

```text
State
→ Senatorial District
→ Federal Constituency
→ LGA
→ Ward
→ Polling Unit
```

The frontend selector queries the local Nigeria GeoData database.

## Submissions

Submissions are stored locally in WordPress and can be reviewed under:

```text
Nigeria GeoData → Submissions
```

Administrators can inspect submission details and export records as CSV.

## Notifications

GeoForms supports:

- administrator notification email
- optional submitter confirmation email
- configurable success message

## Validation

Geographic selections are validated server-side against the local relationship graph before the submission is stored.

## Styling

GeoForms uses semantic HTML and lightweight CSS. Themes and custom CSS can restyle fields, typography, borders, buttons, spacing and layout without changing plugin core files.
