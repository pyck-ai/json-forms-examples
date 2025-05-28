# JSON Forms Examples
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fpyck-ai%2Fjson-forms-examples.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fpyck-ai%2Fjson-forms-examples?ref=badge_shield)


This repository provides examples of JSON Schemas used to generate forms dynamically. The examples are based on the [JSON Schema](https://json-schema.org) standard and demonstrate various ways to structure and validate form data.

## Getting Started

1. You can simply fetch the directory contents using the GitHub API:
   ```sh
   curl https://api.github.com/repos/pyck-ai/json-forms-examples/contents/
   ```
2. Filter for the entries with the `type == dir`.
3. In there you can find the `dataSchema.json` and `uiSchema.json` files for further processing. So just fetch them by replacing `example1` via:
```sh
   curl https://raw.githubusercontent.com/pyck-ai/json-forms-examples/refs/heads/main/example1/uiSchema.json
   curl https://raw.githubusercontent.com/pyck-ai/json-forms-examples/refs/heads/main/example1/dataSchema.json
   ```
3. Use a JSON Schema-based form renderer (e.g., [React JSON Schema Form](https://github.com/rjsf-team/react-jsonschema-form) or [JSONForms](https://jsonforms.io/)) to visualize the forms.

## Example JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "properties": {
    "name": {
      "type": "string",
      "title": "Full Name",
      "minLength": 2
    },
    "age": {
      "type": "integer",
      "title": "Age",
      "minimum": 18
    },
    "email": {
      "type": "string",
      "format": "email",
      "title": "Email Address"
    }
  },
  "required": ["name", "age", "email"]
}
```

## Running the Examples

To render and test the example schemas, you can use:
- [JSON Schema Validator](https://www.jsonschemavalidator.net/)
- [JSONForms](https://jsonforms.io/)
- [React JSON Schema Form Sandbox](https://rjsf-team.github.io/react-jsonschema-form/)

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.



[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fpyck-ai%2Fjson-forms-examples.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fpyck-ai%2Fjson-forms-examples?ref=badge_large)