---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "passbolt Provider"
subcategory: ""
description: |-
  
---

# passbolt Provider



## Example Usage

```terraform
# Basic configuration
provider "passbolt" {
  base_url    = "https://example.passbolt.com"    # PASSBOLT_URL
  private_key = "<YOUR PASSBOLT PGP PRIVATE KEY>" # PASSBOLT_KEY
  passphrase  = "<YOUR PASSBOLT PASSPHRASE>"      # PASSBOLT_PASS
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `base_url` (String) Your Passbolt URL (e.g. `https://example.passbolt.com`). Can also be provided via the `PASSBOLT_URL` environment variable.
- `passphrase` (String, Sensitive) Your Passbolt passphrase associated with your private key. Can also be provided via the `PASSBOLT_PASS` environment variable.
- `private_key` (String, Sensitive) Your Passbolt PGP Private Key. Can also be provided via the `PASSBOLT_KEY` environment variable.