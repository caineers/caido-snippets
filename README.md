# Caido Snippets
## 🔎 Filters presets [^1]
### No Browser's own request
```lua
(req.host.ncont:"safebrowsing.googleapis.com" AND 
(req.host.ncont:"detectportal.firefox.com" AND 
(req.host.nregex:".*.mozilla.(com|org|net)" AND 
(req.host.ncont:"spocs.getpocket.com" AND 
(req.host.ncont:"update.googleapis.com" AND 
(req.host.ncont:"optimizationguide-pa.googleapis.com" AND 
(req.host.ncont:"content-autofill.googleapis.com" AND 
(req.host.ncont:"clients4.google.com" AND 
(req.host.ncont:"clients2.google.com" AND 
(req.host.ncont:"msftncsi.com" AND 
(req.host.ncont:"msftconnecttest.com" AND 
(req.host.ncont:"edge.microsoft.com" AND 
(req.host.ncont:"apple.com" AND 
(req.host.ncont:"icloud.com" AND 
(req.host.ncont:"content-signature-2.cdn.mozilla.net" AND 
(req.host.ncont:"normandy.cdn.mozilla.net" AND 
(req.host.ncont:"versioncheck-bg.addons.mozilla.org")))))))))))))))))
```

[^1]: Sidebar > filters

### Only `Set-Cookie`
```lua
resp.raw.regex:"(?i)Set-Cookie:"
```

### Only Redirects
```lua
(resp.raw.regex:"(?i)Location: " OR (resp.code.eq:301 OR (resp.code.eq:302 OR (resp.code.eq:307 OR resp.code.eq:308))))
```

### Hide `.js`
```lua
req.ext.ncont:"js"
```

## 🤖 Assistant prompts [^2]
[^2]: Sidebar > assistant

## 🔩 GraphQL snippet [^3]
[^3]: Topbar > User > GraphQL Playground

## 🪄 Trick
### Get AccessToken

```javascript
console.log(JSON.parse(localStorage.CAIDO_AUTHENTICATION).accessToken)
```

> AccessToken is used in the Authorization header of Caido's GraphQL, etc.
