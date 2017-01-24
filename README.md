Graylog-Collector

=========

This role installs and configures the graylog sidecar collector.

https://github.com/andhersonsilva/playbook-graylog-collector

Requirements
------------

- RedHat 7 
- Debian 8

Role Variables
--------------

```yaml

## Set up your graylog server name/ip
graylog_server: graylog

## The install method: "yes" = download the package "no" = install from local source
graylog_download_package: "no" 

## Set the package name and url, the variable is located in vars/ in a file according to the OS.
graylog_package_name: collector-sidecar_0.1.0-1_amd64.deb
graylog_package_url: https://github.com/Graylog2/collector-sidecar/releases/download/0.1.0-beta.3/{{graylog_package_name}}

## Source folder on the ansible server where the package are in 
graylog_package_source_folder:  /srv/files/

## Destination folder on the target host to the package
graylog_package_folder: /usr/local/src

## Configure tags , one per line.
graylog_tags:
   - linux

```

Dependencies
------------


Example Playbook
----------------

License
-------

BSD

Author Information
------------------

By Andherson Silva(andherson@gmail.com)
