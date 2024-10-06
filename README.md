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

## Testing

The test-env folder contains the docker-compose file from https://woodpecker-ci.org/docs/administration/deployment-methods/docker-compose and an env template file with the necessary keys and instructions on getting the values.

* Add a hosts file entry of `127.0.0.1  woodpecker.local`
* Copy .env.template to .env
* Populate values
* Launch with `docker compose -f test-env/docker-compose.yml up`
* Visit http://woodpecker.local:8000
* Authorize with GitHub
* Add your repository
