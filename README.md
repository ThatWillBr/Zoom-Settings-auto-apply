# Zoom Settings Auto-Apply

Two browser userscripts for exporting and applying Zoom account settings.

- **Applier.txt** — Zoom Settings Applier v9.1. Loads exported settings JSON and applies settings and lock states through the Zoom account settings interface.
- **Reader & Exporter.txt** — Zoom Settings Reader & Exporter v3.2.0. Reads settings and exports a JSON file compatible with the applier.

## Usage

1. In a userscript manager such as Tampermonkey, create a script for each `.txt` file and paste its complete contents, including the userscript header. Save both scripts.
2. Sign in to Zoom with permission to manage account settings and open `https://zoom.us/account/setting`.
3. Use the reader to read settings, then choose **Export JSON**. Keep a copy of the destination account's settings before applying changes.
4. Use **Load settings JSON** in the applier to select the desired export, then run the apply action.
5. Review the script log and verify the resulting settings in Zoom, including any items reported as not found.

The applier also matches Zoom account integration pages. Both scripts support Zoom subdomains through their userscript match rules.

## Notes

These scripts automate the Zoom website and depend on its page structure, available settings, and account permissions. Applying an export changes account settings and may change lock states. Keep exports private; they can contain account-specific configuration.

The original script files are preserved as provided. JavaScript syntax was checked before publication; live Zoom behavior was not tested as part of publication.
