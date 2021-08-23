## Домашняя работа к занятию “Ansible”

## **LOG**:

``` [root@main home]# ansible-playbook ansible/group_vars/install.yaml -i ansible/inventory
[WARNING]:  * Failed to parse /home/ansible/inventory with yaml plugin: We were unable to read either as JSON nor YAML, these are the errors we got
from each: JSON: No JSON object could be decoded  Syntax Error while loading YAML.   did not find expected <document start>  The error appears to be
in '/home/ansible/inventory': line 2, column 1, but may be elsewhere in the file depending on the exact syntax problem.  The offending line appears
to be:  [all] node1 ansible_host=192.168.1.61 ansible_user=ansible ansible_password=ansible ^ here
[WARNING]:  * Failed to parse /home/ansible/inventory with ini plugin: /home/ansible/inventory:6: Expected key=value host variable assignment, got:
ansible_host:
[WARNING]: Unable to parse /home/ansible/inventory as an inventory source
[WARNING]: No inventory was parsed, only implicit localhost is available

PLAY [netology-ml] **********************************************************************************************************************************

TASK [Gathering Facts] ******************************************************************************************************************************
ok: [node2]
ok: [node1]

TASK [Task ping] ************************************************************************************************************************************
ok: [node2]
ok: [node1]

TASK [Task yum update] ******************************************************************************************************************************
ok: [node1]
ok: [node2]

TASK [Installing package] ***************************************************************************************************************************
ok: [node2]
ok: [node1]

TASK [Task yum update] ******************************************************************************************************************************
ok: [node1]
ok: [node2]

TASK [Copy File] ************************************************************************************************************************************
ok: [node2]
changed: [node1]

TASK [Create Groups] ********************************************************************************************************************************
ok: [node1] => (item=devops_1)
ok: [node2] => (item=devops_1)
ok: [node2] => (item=test_1)
ok: [node1] => (item=test_1)

TASK [Create User] **********************************************************************************************************************************
ok: [node1] => (item={u'client_name': u'devops_1', u'home_dir': u'devops_1'})
ok: [node2] => (item={u'client_name': u'devops_1', u'home_dir': u'devops_1'})
ok: [node1] => (item={u'client_name': u'test_1', u'home_dir': u'test_1'})
ok: [node2] => (item={u'client_name': u'test_1', u'home_dir': u'test_1'})

PLAY RECAP ******************************************************************************************************************************************
node1                      : ok=8    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
node2                      : ok=8    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```