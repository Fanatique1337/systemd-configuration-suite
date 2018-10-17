# systemd-configuration-suite
A group of python scripts used to semi-automate systemd configurations for service, network, timer, slice, and other units

Current version only works for systemd service units (.service files).

**Required systemd currently is *232***

**Usage:**
```
usage: service-config [-h] [-c SCHEMA] [--edit] [--info] [-b] [-s | -x]
                         [-d DIRECTORY] [--delete] [--no-color]
                         [service_name]

Systemd services configuration script

positional arguments:
  service_name          The name of the service to configure/edit.

optional arguments:
  -h, --help            show this help message and exit
  -c SCHEMA, --schema SCHEMA
                        Choose a custom schema and load defaults from it.
  --edit                Directly edit a systemd unit file.
  --info                Show information about the script.
  -b, --build           Builds a default schema in schemas/default-schema
  -s, --short           Use a short configuration schema.
  -x, --extended        Use a long configuration schema.
  -d DIRECTORY, --directory DIRECTORY
                        Output directory for the service unit file.
  --delete              Delete the specified service's configuration file.
  --no-color            Disable colored output.
```

#### Examples:

1. Create a service with name "**test**":
`service-config test`

2. Create a service using an extended schema:
`service-config -x test`

3. Create a service using a short schema:
`service-config -s test`

4. Edit a service:
`service-config --edit <service_name>`

5. Delete a service:
`service-config --delete <service_name>`

6. Create a service in a custom path/directory (using /home/user in the example):
`service-config -d /home/user <service_name>`

For questions and suggestions:
forcigner@gmail.com
