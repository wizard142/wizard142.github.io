# Aibel Shibin’s personal site

A self-contained static site for GitHub Pages. All styles, content, and editor code are in `index.html`; no installation or build is needed.

## Edit and publish

1. Open the site and select **Edit this site** in the footer.
2. Click outlined text to edit your name, introduction, section headings, entries, labels, or footer.
3. Use **+ Section** to add an achievements list, text section, project cards, or contact links. Section controls add text, entries, or links, move sections, and remove sections. Individual content controls move or remove blocks. **Edit link** updates a link’s label and destination.
4. **Undo** reverses edits during the current editing session. Removal requires confirmation.
5. Changes save as a local draft in your browser. After reopening the page, select **Restore draft** to resume. Drafts are specific to the browser and version of the page; download your work before clearing browser data or replacing the site.
6. Select **Publish to GitHub**. The first time in each tab, connect a GitHub fine-grained personal access token with access to only `wizard142/wizard142.github.io` and **Contents: Read and write**. The dialog links to GitHub’s token creation page. Choose an expiry date and paste the token into the password field on your own site.
7. Select **Publish changes** to commit the edited page directly to `main`. GitHub Pages deploys it using the existing repository configuration; deployment may take a few minutes. Subsequent publishes in the same tab reuse the connection. **Disconnect** clears it.
8. **Download site** remains available to save a complete backup. Manual file replacement is optional.

**Done** exits editing to view your local changes. It does not publish them. Visitors can change their own local copy, but publishing requires GitHub repository write access. The publishing token stays in JavaScript memory for the current tab, is sent only to `api.github.com`, and is excluded from drafts and downloaded/published HTML. Closing or reloading the tab disconnects it. Do not paste tokens into editable site text. Revoke expired or unwanted tokens in GitHub settings. The downloaded file includes the editor, so you can keep editing future versions without installing anything.

## Develop locally

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Run from the repository directory and open the site in a browser. The page uses system fonts and does not require external assets.

## Publishing safeguards

The editor checks the page revision and original content against GitHub before writing, and uses GitHub’s file SHA to reject concurrent updates. If the remote page changed, keep a downloaded backup and reload the latest deployment before reapplying your changes. A failed publish leaves the local draft intact. Protected branches and missing write permission can prevent publishing; the dialog reports the error. A successful commit confirms the GitHub update, not completion of the Pages deployment.
