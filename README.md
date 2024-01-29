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
```

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