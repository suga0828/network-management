# CentOS Stream 9

## Installation

1. Download the ISO on [centos.org](https://centos.org/download/) based on your architecture.
2. [Verify the download using the the checksum file](./tutorials/install-centos/README.md#verify-hash).
3. [Install the OS using the ISO as a Virtual Machine using Virtual Box](./tutorials/install-centos).
4. [Install LAMP Stack](./tutorials/install-LAMP-stack).
5. [Install Zabbix](./tutorials/install-zabbix/).
6. [Install Zabbix Agent on Windows](./tutorials/install-zabbix-agent-windows/).
7. [Install Postfix Gmail](./tutorials/install-postfix-gmail/).
8. [Create an alert triggered by Zabbix Agent](./tutorials/trigger-alert-zabbix).
9. [Install and Configure SNMPv3 on CentOS](./tutorials/install-config-SNMPv3/).

---

## Development

To run docs locally, install <a href="https://www.mkdocs.org/getting-started/" target="_blank">MkDocs</a>, the theme <a href="https://squidfunk.github.io/mkdocs-material/" target="_blank">Material for MkDocs</a> and the plugin <a href="https://github.com/oprypin/mkdocs-same-dir" target="_blank">mkdocs-same-dir</a>.

##### Installation

```bash
  pip install mkdocs mkdocs-material mkdocs-same-dir
```

##### Execution

```bash
  mkdocs serve
```

##### Deployment

```bash
  mkdocs gh-deploy
```
