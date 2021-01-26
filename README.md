# Multiple AWS accounts

How do you target different/multiple AWS accounts?

## Switch by profile

Override Environment variables for a command, e.g. profiles.

```shell
$ AWS_PROFILE=default ansible-playbook multi.yml
$ AWS_PROFILE=sa ansible-playbook multi.yml
```

## switch using inventories

Each Environment has its own variables, in this case using profile names.

```shell
$ ansible-playbook test.yml -i inventories/default
$ ansible-playbook test.yml -i inventories/sa
```
