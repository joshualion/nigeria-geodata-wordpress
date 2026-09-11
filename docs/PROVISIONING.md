# Purchase & Provisioning

Nigeria GeoData separates the WordPress plugin from the paid geography provisioning service.

The plugin is GPL-licensed. Paid provisioning is delivered through CampaignManager.ng.

## Available coverage scopes

Customers may provision:

- National
- State / FCT
- Senatorial District
- Federal Constituency
- LGA / Area Council

Live pricing is shown in the plugin administration interface and on CampaignManager.ng.

## Purchase flow

1. Open **Nigeria GeoData → Dashboard** or **Coverage & Expansion**.
2. Follow the purchase link to CampaignManager.ng.
3. Choose the required geography scope.
4. Select the relevant State, constituency or LGA where applicable.
5. Enter the WordPress site URL.
6. Complete payment.
7. After successful payment confirmation, CampaignManager.ng automatically issues a site-bound `NGWP-...` provisioning key.
8. Return to WordPress and enter the key.
9. Start provisioning.

## Resumable provisioning

Provisioning is performed in batches.

If the browser refreshes, the network drops or the process is interrupted, the plugin stores progress locally and can resume from the last successful checkpoint.

The key is consumed only after successful completion.

## Additive coverage

A site can add more geography later.

```text
LGA A
+ LGA B
= both LGAs stored locally
```

```text
Several LGAs
+ State package
= existing overlapping records reused + missing State geography added
```

```text
State package
+ National
= existing State records reused + remaining Nigerian geography added
```

Successful coverage is not deleted because another package is provisioned.

## National coverage

National coverage is the terminal geography scope. Once a completed National package exists, the plugin no longer prompts the site to buy another geography package.

## After provisioning

Data Explorer, shortcodes, REST/PHP/JavaScript APIs, GeoForms and Contact Form 7 selectors use the local WordPress database.
