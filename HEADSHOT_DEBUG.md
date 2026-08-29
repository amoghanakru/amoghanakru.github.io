# Headshot troubleshooting

The home page now requests:

`./assets/AA_headshot.jpeg?v=20260828`

The query string forces browsers/CDNs to request a fresh copy while leaving the actual filename unchanged.

If the image still does not appear:

1. Open the live site, right-click, choose **View Page Source**, and search for `AA_headshot.jpeg`.
   - If it is absent, GitHub Pages is serving a different branch/folder/commit than the file you edited.
2. In the live page, open Developer Tools → **Network**, reload, and click the `AA_headshot.jpeg` request.
   - `200` means the image is loading; inspect the Elements/Computed panel for size/visibility.
   - `404` means the deployed path/filename does not match.
3. In Repository → Settings → Pages, verify the source is the same branch/folder where `index.html` and `assets/AA_headshot.jpeg` exist.
4. In Repository → Actions, open the latest `pages build and deployment` run and verify its commit hash matches the commit containing the new image.
5. If you are using a custom domain, test the default `<username>.github.io` address too. A CDN/custom-domain cache can lag independently.
