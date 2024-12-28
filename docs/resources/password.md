---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "passbolt_password Resource - passbolt"
subcategory: ""
description: |-
  Defines a Passbolt Secret.
---

# passbolt_password (Resource)

Defines a Passbolt Secret.

## Example Usage

```terraform
# Basic Configuration
resource "random_password" "basic" {
  length = 16
}

resource "passbolt_password" "basic" {
  name     = "Basic Password Example"
  username = "myUser"
  password = random_password.basic.result
  uri      = "https://example.com"
}

# Full Password Cofiguration
resource "passbolt_password" "full" {
  name          = "Full Password Example"
  description   = "A Description for the secret."
  username      = "myUser"
  password      = random_password.basic.result
  uri           = "https://example.com"
  share_group   = "SomeShareGroup"
  folder_parent = "Parent Folder"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) The name of the secret.
- `password` (String, Sensitive) The secret password, stored as a sensative string in state.
- `uri` (String) The URI of the secret.
- `username` (String) The username of the secret.

### Optional

- `description` (String) The description of the secret
- `folder_parent` (String) The parent folder in which to place the secret.
- `folder_parent_id` (String) The ID of the parent folder, if `folder_parent` is specified.
- `share_group` (String) The Group Name to share the secret with.

### Read-Only

- `id` (String) The Resource ID of the secret.