### Ansible role for managing docker secrets.

Usage

Run the role in a inventory:

```yaml
ansible-playbook -i inventory/ playbook/docker-secrets.yml
```

##### Example usage:
- Create a Secret
```yaml
docker_secrets:
     API_KEY:
      data: uLgdSLDq98eQxMTj
      state:  present
```

- Delete a Secret
```yaml
docker_secrets:
     API_KEY:
      data: uLgdSLDq98eQxMTj
      state:  absent
```
### Example

Create a playbook called `docker-secrets.yml`
```yml
- hosts: all
  gather_facts: false
  become: true
  role:
    - jobin_james.docker_secrets
```
