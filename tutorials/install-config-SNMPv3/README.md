# Install and Configure SNMPv3 on CentOS

## Steps to configure SNMPv3

##### 1. Install the required packages

Install the 2 required packages namely,

1. net-snmp-utils
2. net-snmp-devel

```
# yum install net-snmp net-snmp-utils net-snmp-devel
```

net-snmp-utils is required to use the utility snmpwalk.

##### 2. Configure SNMP version 3 user

1. Turn off the service.
   We need to turn off the agent when running net-snmp-create-v3-user command.

```
# service snmpd stop
```

2. Create the user.
   Then we run the following command:

```
#  net-snmp-config --create-snmpv3-user -ro -A SHApassword -X AESpassword -a SHA -x AES username
```

The syntax of –create-snmp3-user is as below :

- --create-snmpv3-user [-ro] [-A authpass] [-X privpass] [-a MD5|SHA] [-x DES|AES] [username]
- Default authentication method is MD5 and default encryption is DES if not explicitly specified.

The sample username is `username`, SHA password is `SHApassword`, and AES password is `AESpassword`.

3. Start the service.
   Use chkconfig command to configure the SNMP services to start on each reboot :

```
# chkconfig snmpd on
```

Start the snmpd service :

```
# service snmpd start
```

4. Test the setup using snmpwalk command

```
# snmpwalk -v3 -u username -l authPriv -a SHA -A SHApassword -x AES -X AESpassword localhost

```

Here,

- -v3 - specifies version
- -u - specifies username
- -l - specifies security level
- -a - specifies Authentication Protocol
- -A - specifies Pass-phrase
