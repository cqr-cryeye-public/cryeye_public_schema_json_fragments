# Fragments: Schema JSON

Fragments this is a system of data extraction from source data.

You can make this, with usage of special "schema". For now, it is recommended to use "yaml" format for this.

For simpler usage, you can use "json-schema" for validation of "fragments" schema.

## Usage

### 🌐 By url

Add to the top of your "yaml" file something like this:

```yaml
# yaml-language-server: $schema=https://raw.githubusercontent.com/OWNER/REPOSITORY/BRANCH/PATH
```

So, this will be something like this:

```yaml
# yaml-language-server: $schema=https://raw.githubusercontent.com/cqr-cryeye-public/cryeye_public_schema_json_fragments/v0.1.0/schema/fragments.schema.json
---
engine:
  version: 0.1.0
meta:
  version: 1.0.0
schema:
  fragments:
    - type: many
      getter: { type: nested, query: values }
      config:
        info: { title: Value, description: Extracted values }
        fields:
          - { key: value, type: text }
```

Note:

If you use JetBrains IDE, and need to reload used schema for file, you can restart the IDE. Or, you can make this:

1. In JetBrains IDE, go to: `File` -> `Invalidate Caches...`.
2. Click "Just Restart" button.

After this, all instances of IDE will be restarted.


### 📝 By file

Place somewhere file with `fragments.schema.json`.

1. In JetBrains IDE, go to: `File` -> `Setting`.
2. Then go to: `Languages & Frameworks` -> `Schemas & DTDs` -> `JSON Schema Mappings` (or try to search last part).
3. Click the `+` icon to add a new mapping.
4. Give the new mapping the name `Data fragments YAML Schema`.
5. Provide a path to `fragments.schema.json`.
6. Select `Schema version` to `JSON Schema version 7`.

7. Click the new `+` icon. Select `Add file path pattern`.
8. Add pattern `*/schema.yaml`.

9. Click "Accept" and/or "OK" to close the settings window.