# dbrennand.beszel

Ansible role to install and configure a [Beszel](https://github.com/henrygd/beszel) binary agent.

## Requirements

None.

## Role Variables

```yaml
beszel_public_key: ""
```

Public key used to authenticate the Beszel binary agent to the Hub.

```yaml
beszel_state: present
```

State of the Beszel binary agent installation. Can be either `present` or `absent`.

```yaml
beszel_version: latest
```

Version of the Beszel binary agent to install. Can be a specific version from GitHub (e.g., `v0.9.1`).

```yaml
beszel_port: 45876
```

Port for the Beszel binary agent to listen on.

```yaml
beszel_install_dir: /usr/local/bin
```

Directory to install the Beszel binary agent into.

```yaml
beszel_args: ""
```

Custom arguments for the Beszel binary agent.

```yaml
beszel_service_enabled: true
```

Enable the Beszel binary agent systemd service on boot.

```yaml
beszel_service_state: started
```

State of the Beszel binary agent systemd service.

## Dependencies

This role depends on a precompiled binary published on GitHub at [henrygd/beszel](https://github.com/henrygd/beszel/releases/tag/v0.9.1)

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: dbrennand.beszel
      vars:
        beszel_public_key: "<Public key for Beszel hub>"

```

## License 📝

[LICENSE](LICENSE).

## Contributors

[dbrennand](https://github.com/dbrennand)
