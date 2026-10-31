![Banner](banner.png)

# misconfig-ConfigSchemaValidator
A command-line tool that validates configuration files against a predefined schema (e.g., JSON Schema or YAML schema) to ensure data types and required fields are correct. Uses the `jsonschema` library for JSON and `ruamel.yaml` for YAML validation. - Focused on Check for misconfigurations in configuration files or infrastructure definitions

## Install
`git clone https://github.com/ShadowStrikeHQ/misconfig-configschemavalidator`
`pip install -r requirements.txt`

The requirements name the `ruamel.yaml` distribution, which provides the `ruamel.yaml` import the tool uses, along with `jsonschema`. Both install steps are required: cloning alone does not install the libraries, and the tool cannot start without them.

## Usage
`python3 main.py <config_file> <schema_file> [--config_type json|yaml] [--schema_type json|yaml] [--log_level INFO]`

An empty config file or an empty schema file is reported by name as an empty file and exits 1, rather than failing with an internal library message.

## Parameters
- `-h`: Show help message and exit
- `config_file`: Path to the configuration file (JSON or YAML).
- `schema_file`: Path to the schema file (JSON or YAML).
- `--config_type`: Specify config file type (JSON or YAML). If not specified, it is guessed from the extension.
- `--schema_type`: Specify schema file type (JSON or YAML). If not specified, it is guessed from the extension.
- `--log_level`: Set the logging level.

## License
Copyright (c) ShadowStrikeHQ
