# OrcaFarm Etsy callback

Standalone static callback landing page for OrcaFarm's current manual OAuth return flow. This is not the desktop UI. Publish only this directory in a separate public repository; never publish the private application repository, credentials or customer records.

Proposed repository: zachpeterson5/orcafarm-etsy-callback
Proposed callback (not live until publication is verified):
https://zachpeterson5.github.io/orcafarm-etsy-callback/callback.html

Use the exact published URL in both the Etsy app's redirect registration and OrcaFarm. The static page does not inspect the query string or exchange tokens. Users copy the complete callback URL to the native app, which verifies state, destination and PKCE. GitHub receives the HTTP request, including its query string; PKCE keeps token exchange dependent on the verifier retained in the desktop session. There are no scripts, remote assets, analytics or forms. The no-referrer policy prevents outgoing referrer disclosure.

Publish from main / (root) with GitHub Pages. Verify HTTPS returns this page without redirecting to a different callback path. Test the page with no credentials; real authorization requires explicit user approval in Etsy.
