Ansible Role for MongoDB
====================

[![Build Status](https://travis-ci.org/vitalied/ansible-role-mongodb.svg?branch=master)](https://travis-ci.org/vitalied/ansible-role-mongodb)
[![GitHub tag](https://img.shields.io/github/tag/vitalied/ansible-role-mongodb.svg)](https://github.com/vitalied/ansible-role-mongodb)
[![GitHub license](https://img.shields.io/github/license/vitalied/ansible-role-mongodb.svg)](https://github.com/vitalied/ansible-role-mongodb/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/9294.svg)](https://galaxy.ansible.com/vitalied/mongodb)

Ansible Role for MongoDB Management.

Requirements
------------

This role require Ansible 2.1 or higher.

This role was designed for Ubuntu Server 14.04+.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>mongodb_data_dir</td>
<td>yes</td>
<td>/srv/mongodb</td>
<td></td>
<td>Specifies the mongodb data storage directory.</td>
</tr>
<tr class="even">
<td>mongodb_journal_enabled</td>
<td>yes</td>
<td>true</td>
<td><ul>
<li>true</li>
<li>false</li>
</ul></td>
<td>Enable or disable the durability journal to ensure data files remain valid and recoverable.</td>
</tr>
<tr class="odd">
<td>mongodb_bind_ip</td>
<td>yes</td>
<td>127.0.0.1</td>
<td></td>
<td>
  The IP address (127.0.0.1 for localhost) on which mongodb will listen for requests.
  Set to 0.0.0.0 to listen on all interfaces.
  To bind to multiple IP addresses, enter a list of comma separated values.
</td>
</tr>
<tr class="even">
<td>mongodb_port</td>
<td>yes</td>
<td>27017</td>
<td></td>
<td>The port on which mongodb will listen for requests.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: vitalied.mongodb

License
-------

-   Code released under [MIT](https://github.com/vitalied/ansible-role-mongodb/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)
