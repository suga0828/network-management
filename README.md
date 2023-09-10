# Get Started

The next tutorials will cover a set of configuration commonly used in Network Monitoring. These tutorials are made to be followed on CentOS 9 Stream.

## Tutorials

1. [Install CentOS 9 Stream](./tutorials/install-centos) on a virtual machine using Virtual Box.
2. [Install LAMP Stack](./tutorials/install-LAMP-stack) on CentOS 9 Stream.
3. [Install Network Monitoring Solution Zabbix](./tutorials/install-zabbix/) on CentOS 9 Stream.
4. [Install Zabbix Agent](./tutorials/install-zabbix-agent-windows/) on Windows.
5. [Install and configure Postfix to use Gmail SMTP](./tutorials/install-postfix-gmail/) on CentOS 9 Stream.
6. [Create and configure Zabbix Agent's alert](./tutorials/trigger-alert-zabbix-agent).
7. [Install and configure SNMPv3](./tutorials/install-config-SNMPv3/) on CentOS 9 Stream.

---

## Development

To run docs locally, install <a href="https://www.mkdocs.org/getting-started/" target="_blank">MkDocs</a>, the theme <a href="https://fernandocelmer.github.io/mkdocs-simple-blog/" target="_blank">MkDocs Simple Blog</a> and the plugin <a href="https://github.com/oprypin/mkdocs-same-dir" target="_blank">mkdocs-same-dir</a>.

##### Installation

```bash
pip install mkdocs mkdocs-simple-blog mkdocs-same-dir
```

##### Execution

```bash
mkdocs serve
```

##### Deployment

```bash
mkdocs gh-deploy
```
