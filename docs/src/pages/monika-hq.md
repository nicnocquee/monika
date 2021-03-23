---
id: monika-hq
title: Monika-HQ
---

`monika-hq` is a web app to manage multiple instances of Monika locally and remotely. 

![](/monika/monika-hq.png)

# Getting started

1. Install monika-hq: `npm i -g @hyperjumptech/monika-hq`
2. Run in port 8080: `monika-hq -p 8080`
3. Open browser and go to http://<IP_OF_MONIKA_HQ>:8080
4. Create a Monika API Key. Provide a `name` and then click `Generate`.

Next, we need to run Monika with the `monika-hq`'s URL and the generated key as follows.

1. Update Monika's config.json with the generated key as follows

    ```json
    {
        "monika-hq": {
            "url": "MONIT_HQ_URL",
            "key": "GENERATED_KEY"
        }
    }
    ```

2. Run `monika -c config.json`.

Now Monika will regularly send reports to Monika-HQ. Then you can see the report from the Monika-HQ web app.

# Features

## Probe Management

- Show list of probes

## Manage Monika API Keys

- Create new key
- Disable a key
- Delete a key
- Show list of keys: Instances of Monika that are using the key and when it was last used.