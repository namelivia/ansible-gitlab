# Gitlab Ansible role [![Ansible Lint](https://github.com/namelivia/ansible-gitlab/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/namelivia/ansible-gitlab/actions/workflows/ansible-lint.yml)

## This is a WIP

The project depends on the collection `community.docker` but apparently this [cannot be listed as a dependency](https://github.com/ansible/ansible/issues/62847) so make sure you add it to your `requirements.yml` file like:

```yml
---

collections:
  - community.docker

roles:
  - src: https://github.com/namelivia/ansible-gitlab
```

## Required variables
 - `cloudwatch_region` Cloudwatch region to send the logs to.
 - `cloudwatch_log_group` Cloudwatch log group to send the logs to.
 - `domain_name` Domain name in which gitlab will be served from.
 - `backup_day` Day of the week in which the content will be backed up.
