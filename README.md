# Foundry VTT MCP — public releases

Installation downloads for the Foundry VTT MCP Bridge: a Foundry v14+ module and a local MCP companion, with 51 tools for campaign preparation and bounded live play. General tools are system agnostic; the optional Pathfinder 2e adapter uses native system APIs.

## Install in Foundry

In Foundry Setup, open **Add-on Modules → Install Module**, then paste this Manifest URL:

```text
https://github.com/Tommo999/foundry-vtt-mcp-releases/releases/latest/download/module.json
```

The manifest points to a version-specific `foundry-vtt-mcp.zip`. Foundry can check this stable manifest URL for future releases using its normal module Update controls. A Git commit or tag alone does not publish an update: the release assets and their versioned manifest must be published.

If the bridge was installed manually without update URLs, replace its existing files once using the named module ZIP in this repository's Releases. The destination is the Foundry host's `Data/modules/foundry-vtt-mcp` directory, containing `module.json`, `module.js` and `module.css`. Stop the world while replacing package files, then reload/restart Foundry as needed. Keep companion configuration, certificates and pairing intact; do not initialize a new pairing just to update.

## Companion and Windows setup

Download `foundry-vtt-windows-setup.zip` from Releases, extract it into a writable folder, and run `setup-windows.cmd` on Windows. The bundle includes installation and security documentation plus the application source needed to build it. Node.js 22.12 or later and a trusted localhost certificate are required.

**Foundry's module Update button does not update the companion.** Update the companion from the matching version of the setup/source bundle, preserve its existing configuration/certificates/pairing, restart it, and refresh the GM browser. Keep the GM browser open and connected to the intended world. The companion runs beside the GM browser/MCP client; the Foundry Docker container needs no new exposed companion port.

## Verification and testing

Each release includes `SHA256SUMS.txt` for the standalone manifest and both named ZIPs. Verify these checksums after downloading. GitHub's automatically generated Source code ZIP/TAR contains only this distribution repository; use the named release assets for installation.

Test changes with an explicitly chosen release in a separate Foundry instance/data directory before updating a campaign. The stable manifest follows the latest normal release; prerelease/draft builds are not a separate automatic update channel. Current targeted live validation of the v0.8.1 search, encounter-reporting and ammunition repairs remains pending; automated tests do not establish compatibility across Foundry/PF2e versions.

This repository hosts public release downloads and installation information. Development history, test trees, live acceptance reports, campaign fixture identifiers, companion credentials and TLS private keys are not included in the release assets. The Windows setup bundle does include selected application source files. Source-hosting privacy does not make distributed application code private.
