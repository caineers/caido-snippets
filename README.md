# Caido Snippets
## Filters presets
### No Browser's own request
```lua
(req.host.ncont:"safebrowsing.googleapis.com" AND (req.host.ncont:"detectportal.firefox.com" AND (req.host.nregex:".*.mozilla.(com|org|net)" AND (req.host.ncont:"spocs.getpocket.com" AND (req.host.ncont:"update.googleapis.com" AND (req.host.ncont:"optimizationguide-pa.googleapis.com" AND (req.host.ncont:"content-autofill.googleapis.com" AND (req.host.ncont:"clients4.google.com" AND (req.host.ncont:"clients2.google.com" AND (req.host.ncont:"msftncsi.com" AND (req.host.ncont:"msftconnecttest.com" AND (req.host.ncont:"edge.microsoft.com" AND (req.host.ncont:"apple.com" AND req.host.ncont:"icloud.com")))))))))))))
```

### Only `Set-Cookie`
```lua
resp.raw.regex:"(?i)Set-Cookie:"
```

## Assistant prompts
.

## GraphQL snippet
.
