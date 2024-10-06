# xmpp-interop-tests-woodpecker-plugin

Woodpecker plugin for testing XMPP interoperability

## Usage

This is used in Woodpecker, like this:

```yaml
  - name: run-xmpp-interop-tests
    image: ghcr.io/xmpp-interop-testing/sintse-woodpecker:main
    settings:
      domain: example.org
      host: 127.0.0.1
      timeout: 5000
      adminAccountUsername: admin
      adminAccountPassword: s3cr3t
      disabledTests: PubSubIntegrationTest
      disabledSpecifications: XEP-0045
```

