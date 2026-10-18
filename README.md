# Velva plugins for Claude

This marketplace contains the [Velva plugin](velva/README.md): one focused creative-production skill and a connection to Velva's hosted MCP server. A Velva account is required; metered operations use the account's credits after a live quote and spending authorization.

## Install

This distribution already includes the complete plugin and its icon. Run from this folder:

```sh
claude plugin marketplace add ./
claude plugin install velva@velva
```

Then enable the Velva MCP server, complete its normal OAuth sign-in, and use `/velva:velva` or ask Claude to work with Velva. See the [plugin README](velva/README.md) for examples, data handling and support.

## Validate

With Claude Code 2.1.281 or newer:

```sh
claude plugin validate ./velva --strict
claude plugin validate . --strict
```

The local validator checks package structure and schemas. Directory submission additionally requires validation in Anthropic's developer portal and a separate submission for the Velva MCP connector. Installing this source marketplace does not establish directory approval.

Velva's application source is not part of this distribution. The [MIT license](velva/LICENSE) applies to the plugin bundle; the hosted Velva service and its content remain subject to their own terms.
