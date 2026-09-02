# Ideas Collide GEO Site

This is a standard static HTML site. It does not require Node, React, npm, or a build command.

The homepage and included subpage template contain a `noindex, nofollow` robots directive. Keep that directive while the site should remain out of search results, and remove it before public indexing is desired.

## Files

- index.html is the homepage and must remain in the repository root.
- assets/site.css contains the site styling.
- assets contains the logo and report graphics.
- subpage-template.html is the starting point for new pages.

## Add a subpage

To create /services/geo-audit/:

1. Create folders named services and then geo-audit.
2. Copy subpage-template.html into services/geo-audit/.
3. Rename the copied file to index.html.
4. Edit its title, description, headline, and page content.
5. Link to it with href="/services/geo-audit/".

## Clean report URLs

The Logicalis report lives at `logicalis/index.html`, so its public URL is `/logicalis/`. This directory-based structure provides clean URLs on Sevalla static hosting without `.htaccess` or Apache rewrite rules. Use the same pattern for future reports: `client-name/index.html` becomes `/client-name/`.

## GitHub

Put the CONTENTS of this folder in the repository root. Do not upload the ZIP itself. GitHub should show index.html, README.md, subpage-template.html, and assets at the top level.

## Sevalla static-site settings

- Branch: main
- Build command: leave blank
- Publish directory: .
- Index file: index.html

Every push to main should trigger a new deployment.
