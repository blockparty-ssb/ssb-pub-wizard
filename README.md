# ssb-pub-wizard

Easily set up a Secure Scuttlebutt pub _for altnet with custom network ID/ caps.shs key on Digital Ocean. Copy your API token, choose server size and region, and let the installer do the rest for you!

This module returns the wizard's HTML and will call back with information about the pub once it's set up. Include it in your application or see it in action in [blockparty](https://github.com/blockparty-ssb/blockparty)

## Usage

```javascript
const wizard = require('ssb-pub-wizard')

const html = wizard((err, pubInfo) => {
  // pubInfo has:
  {
    appId: // the network's caps key,
    port: // port the pub listens on,
    wsPort: // the pub's ws port,
    appName: // name the user chose for the pub,
    keys: // the user's keys generated for this network,
    pubKey: // the pub's public key,
    ip: //the pub's IP
  }
)
```
