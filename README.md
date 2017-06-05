[![Docker Repository on Quay](https://quay.io/repository/aaroc/fg_api/status?token=29400784-71e1-4eb0-8493-0775c34b2464 "Docker Repository on Quay")](https://quay.io/repository/aaroc/fg_api)

# Role Name

Adds a [FutureGateway API](https://github.com/FutureGateway/fgAPIServer) service to your [Ansible Container](https://github.com/ansible/ansible-container) project. Run the following commands
to install the service:

```
# Set the working directory to your Ansible Container project root
$ cd myproject

# Install the service
$ ansible-container install AAROC.fg-api
```

## Requirements

- [Ansible Container](https://github.com/ansible/ansible-container)
- An existing Ansible Container project. To create a project, simply run the following:
    ```
    # Create an empty project directory
    $ mkdir myproject

    # Set the working directory to the new directory
    $ cd myproject

    # Initialize the project
    $ ansible-contiainer init
    ```


## Role Variables

  * `apache_conf_path`: Path to the Apache virtual host configuration files
  * `apache_vhosts_filename`: Specific filename  of the Apache virtual host of the API server
  * `system_prerequisites`: OS-dependent list of prerequisite packages
  * `pip_packages`: Extra pip packages necessary for the API
  * `api_server_repo`, `api_server_branch`: Git repository of the API server application; Branch to clone in the repository
  * `fg_user`: The user which the WSGI interface runs as.
  * `apache_mods_enabled`: Apache modules enabled
  * Variables used in the flask configuration
    * `fgapiver`: Undocumented
    * `fgapiserver_name`: Name of the application
    * `fgapisrv_host`: Host on which the application is running (defaults to localhost)
    * `fgapisrv_port`: Port on which the flask API listens
    * `fgapisrv_debug`: Boolean expressing whether the Flask application runs in debug mode or not.
    * `fgapisrv_iosandbox`: Writeable directory in which the input and output sandboxes are put.
    * `fgapisrv_geappid`: Undocumented
    * `fgjson_indent`: Undocumented
    * `fgapisrv_key`: Undocumented
    * `fgapisrv_crt`: Undocumented
    * `fgapisrv_logcfg`: Undocumented
    * `fg_db_schemaver`: Unducumented
    * `fgapisrv_dbver`: Undocumented
    * `fgapisrv_secret`: Undocumented
    * `fgapisrv_notoken`: (Boolean) Undocumented
    * `fgapisrv_notokenusr`: Undocumented
    * `fgapisrv_lnkptvflag`: (Boolean) Undocumented
    *  `fgapisrv_ptvendpoint`: Undocumented
    * `fgapisrv_ptvuser`: Undocumented
    * `fgapisrv_ptvpass`: Undocumented
    * `fgapisrv_ptvdefusr`: Undocumented
    * `fgapisrv_ptvdefgrp`: Undocumented
    * `fgapisrv_ptvmapfile`: Undocumented

## Dependencies

None

## License

Apache-2.0

## Author Information

Bruce Becker (C.S.I.R. Meraka Institute)
Riccardo Bruno (Universita' di Catania)
