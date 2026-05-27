# grafana

Automates installation, configuration, and state management of Grafana

## Table of contents

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [grafana_actions](#grafana_actions)
  - [grafana_admin_password](#grafana_admin_password)
  - [grafana_admin_user](#grafana_admin_user)
  - [grafana_port](#grafana_port)
  - [grafana_state](#grafana_state)
  - [grafana_version](#grafana_version)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.20`

## Default Variables

### grafana_actions

List of actions the role does, accepts one or more actions.
Use comma without spaces as a delimiter for multiple actions.

**_Required:_** `true`<br />
**_Type:_** String<br />

#### Example usage

```YAML
  grafana_actions: install
  grafana_actions: install,configure,state_control
```

### grafana_admin_password

Grafana admin password

**_Required:_** `true`, only when action is configure<br />
**_Type:_** String<br />

### grafana_admin_user

Grafana admin username

**_Required:_** `true`, only when action is configure<br />
**_Type:_** String<br />

#### Default value

```YAML
grafana_admin_user: admin
```

### grafana_port

TCP port Grafana uses to serve the web interface

**_Type:_** Integer<br />

#### Default value

```YAML
grafana_port: 3000
```

### grafana_state

Target state for the Grafana daemon

**_Required:_** `true`, only when action is state_control<br />
**_Type:_** String<br />

#### Example usage

```YAML
  grafana_state: started
  grafana_state: restarted
```

### grafana_version

Grafana version to be installed

**_Required:_** `true`, only when action is install<br />
**_Type:_** String<br />

#### Default value

```YAML
grafana_version: 12.0.1
```

## Dependencies

None.

## License

MIT

## Author

freedform
