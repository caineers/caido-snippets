# Caido Snippets
## Filters presets
### No Browser's own request
```lua
(req.host.ncont:"incoming.telemetry.mozilla.org" AND (req.host.ncont:"safebrowsing.googleapis.com" AND (req.host.ncont:"firefox.settings.services.mozilla.com" AND (req.host.ncont:"update.googleapis.com" AND (req.host.ncont:"clients4.google.com" AND (req.host.ncont:"clients2.google.com" AND (req.host.ncont:"msftncsi.com" AND (req.host.ncont:"msftconnecttest.com" AND (req.host.ncont:"edge.microsoft.com" AND (req.host.ncont:"apple.com" AND req.host.ncont:"icloud.com"))))))))))
```

## Assistant prompts
.

## GraphQL snippet
.
