# Security scope

PK-lab is a static, client-side educational application. It has no application server, account system, API keys, analytics, or remote data submission. Parameter and language preferences stay in the browser. GitHub provides hosting and receives ordinary website requests.

The October 2026 review hardened saved multiple-dose settings with numeric bounds, finite-number checks and an allowlist. Named scenarios and export functions were subsequently removed from the app. A Content Security Policy blocks external scripts, network connections, plugins, form submissions and base-URL changes; the bundled inline scripts are individually authorized by SHA-256 hashes. Images are limited to same-origin and embedded data. The policy allows inline styles because the app builds interactive SVG and layout styles.

Validation includes malformed saved settings, embedded-script hashes, model regression tests, and browser console checks. This is a focused review, not a guarantee that no vulnerability exists.

Visitors can always alter their own downloaded copy or local browser state. This cannot be prevented by a standalone HTML application and does not modify the hosted file for other visitors. Repository and GitHub account access remain the boundary for changing the public site; account permissions and hosting infrastructure are outside this code review. GitHub Pages controls HTTP response headers, so the HTML cannot add a supported `frame-ancestors` policy or other server-only protections.

Useful background: [OWASP DOM XSS prevention](https://cheatsheetseries.owasp.org/cheatsheets/DOM_based_XSS_Prevention_Cheat_Sheet.html), [MDN Content Security Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CSP).
