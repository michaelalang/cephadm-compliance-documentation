# cephadm-compliance-documentation
Cephadm recording and reporting the utilized calls for compliance documentation

## purpose
This project is intend to *record* the utilized executables from cephadm to report and document them for compliance and security.

Many companies choose a none privileged user deployment for security complaince and separation of various privileged tasks within their Organizations. Reporting the binaries used by cephadm is trying to support the Storage Teams to provide a list of commands and reports for compliance to their Security Teams.


# **NOTE**
```
! The output of commands is not intend to limit sudoers configuration in anyway ! 
Full support from the community or any other Support Provider is only guaranteed by unrestricted and password less sudoers access
```

Furthermore, the list of commands are subject to change by adding/removing functionality in the cephadm tool and therefor shall be used as report with a dedicated deadline/re-evaluation date.

## How to generate a report of the currently used binaries

### prerequisits

* a list of base package binaires
** for YUM/DNF/RPM based distributions the script utilized groupinfo *base* to generate the list
* a working copy of the targeted version of cephadm repository

### calling the reporting script

* change your working directory into the cephadm workspace root directory 

```
$ git clone https://github.com/ceph/ceph.git
[...output omitted...]

$ cd ceph 
```

* copy the cephadm-security-doc binary into you local executable search path (~/bin /usr/local/bin)

```
$ git clone https://github.com/michaelalang/cephadm-compliance-documentation.git
[...ouput omitted...]

$ cp cephadm-compliance-documentation/cephadm-security-doc ~/bin/
$ chmod 0755 ~/bin/cephadm-security-doc
```

* execute the binary to retrive a list of utilized binaries to stdout in your cephadm workspace

```  
$ cephadm-security-doc

..
..
...
```
