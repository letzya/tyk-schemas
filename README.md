# tyk-chemas

**JSON and YAML schemas for various json file types used by Tyk products. 
You can use these schemas in your IDE or favourite editor to get autocompletion and validation of all your Tyk related configuration files.**


**This project is an MVP and still WIP**


## Support Status symbols

| Symbol | Description |
| --------- | --------- |
| ✅ | Fully supported |
| ⚠️ | Untested / Requires Documentation |
| ❌️ | Not currently supported |
| NA | Not available |

## Client to Gateway Authentication

| Type        | JSON      | YAML | Comments |
| ----------- | --------- | ---- | --------- |
| Tyk API definition | ⚠️ | ❌️ | - |
| Tyk API OAS definition | ❌️ | ❌️ | - |
| Tyk key definition | ⚠️ | ❌️ | Also referred as "session object" |
| Tyk policy definition | ❌️ | ❌️ | - |
| Tyk OSS gateway config file | ⚠️ | NA | - |
| Tyk Pro gateway config file | ❌️ | NA | - |
| Tyk hybrid gateway config file | ❌️ | NA | - |

# Usage
To write in "Tyk language" and feel it's native to your IDE config the settings in your IDE to use the JSON schemas in this repository

## VS Code
Edit your settings.json as explained [here](https://code.visualstudio.com/docs/languages/json#_mapping-to-a-schema-in-the-workspace).

Add the following lines to your `setting.json`:

```json
"json.schemas": [
          {
            "fileMatch": [
                "tyk.*.conf"
            ],
            "url": "https://raw.githubusercontent.com/letzya/tyk-schemas/main/schema_tyk.oss.conf"
        },
        {
            "fileMatch": [
                "apikey.*.json"
            ],
            "url": "https://raw.githubusercontent.com/letzya/tyk-schemas/main/schema_apikey.json"
        },
        {
            "fileMatch": [
                "apidef.*.json"
            ],
            "url": "https://raw.githubusercontent.com/letzya/tyk-schemas/main/schema_apidef_lean.json"
        },
    ],
```
and also 
```json
    "files.associations": {
        "*.conf": "json"
    }
```

## Goland


