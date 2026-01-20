# BaulT ZMK Repo

## Instructions

Add this repository to your existing `config/west.yml` as shown below. (No idea what that means? [Check this repository instead!](https://github.com/Armastardo/bault-user-config))

```yaml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    # Add the base GitHub URL as a remote.
    - name: armastardo # You can name this whatever you like; just make sure the "remote" below matches.
      url-base: https://github.com/Armastardo
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    # Add the name of the repository as a project.
    - name: bault-zmk-config
      remote: armastardo
      revision: main # This is the name of the branch you want to use.
  self:
    path: config
```

After doing so, add a copy of [the default keymap](arm/bault/bault.keymap) and create a `bault.conf` file `config` folder that is already in your repo. You can take a look at the [user repo](https://github.com/Armastardo/bault-user-config) for an example.

Note
<br>

[Case](https://github.com/seirin-blu/SK-Vault-35-Case)

