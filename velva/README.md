# Velva for Claude

Use your Velva projects, Library and creative production tools from Claude. This plugin connects to Velva's hosted MCP server and includes guidance for working with professional film and advertising briefs.

## Install from source

In Claude Code, add the marketplace from the source checkout. Run these commands from the folder containing `.claude-plugin/marketplace.json` and `velva/`:

```sh
claude plugin marketplace add ./
claude plugin install velva@velva
```

For a temporary development session with just the plugin folder, run `claude --plugin-dir ./velva` from its parent folder. The included skill is available as `/velva:velva`.

## Connect your account

Install the plugin, enable its Velva MCP server, and complete the OAuth sign-in when Claude asks. Use your normal Velva account. Review the permissions on Velva's consent page before allowing access. The plugin contains no API key, password, local executable or background worker. Claude manages the connection credentials; do not paste credentials into a conversation.

A Velva account is required. Generations and other metered operations use that account's Velva credits. Installing the plugin does not buy credits or subscribe to a plan.

## Examples

- “List my Velva projects and find the latest lighting study.”
- “Quote a 16:9 cinematic product still with hard side light. Show me the price before generating.”
- “Use the approved brief to generate that still for no more than the quoted credits, then show the result.”
- “Check my existing Velva generation job and tell me whether it finished.”

## Working rules

The assistant first reads the tools available on the connected server. It quotes paid work, respects the approved credit ceiling, and follows the returned job ID until it succeeds or fails. A submitted job is not a finished result. It returns the output link and any project or Library location reported by the server. Files and account data are accessed only when needed for the requested work.

The connector and plugin bundle are separate directory submissions. Installation from source does not mean either has passed directory review. Available tools also depend on the permissions granted and on the server release. Use only tools actually declared by the connected server; there is no hidden operation dispatcher.

## Data and service behavior

The bundle contains one skill and one remote MCP connection to `https://velva.ai/mcp`. It installs no dependencies and runs no local scripts, hooks, executables or background workers. It has no independent analytics or storage service.

When Claude calls a Velva tool, it sends that request's arguments and referenced inputs to Velva. Depending on the requested operation and granted permissions, Velva returns account information, project details, Library media, live quotes, job status or output links. The connector does not receive the complete conversation or Claude's memory automatically. Requests can contain personal data, including names, media depicting people and information in a connected account.

Velva may pass the inputs needed for an authorized task to its generation, storage, stock-search or connected-service providers. Sending, posting, scheduling and other external changes require the user's explicit instruction and a declared tool for that operation. Generated and uploaded files, projects, connection records and billing records are retained by the hosted service as explained in the [privacy policy](https://velva.ai/privacy). The plugin does not set a separate retention period.

This plugin is intended for professional creative work by adults. Use of Velva and any generated or third-party media remains subject to the [service terms](https://velva.ai/terms).

## Help and account access

- [Setup, tools and troubleshooting](https://velva.ai/docs/connector)
- [Support](https://velva.ai/support)
- [Privacy](https://velva.ai/privacy)
- [Terms](https://velva.ai/terms)

Manage or revoke the assistant's connection in your Velva account settings. If a permission was not granted, explain the missing permission instead of requesting passwords or switching to another person's account.

The MIT license covers this plugin bundle only. Velva's hosted service, account, credits, generated media and third-party assets remain governed by their applicable terms.
