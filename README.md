Ansible role: Bun (Node.js Alternatives)
=========

Ansible roles to install bun binary globally. [Bun] is a fast JavaScript all-in-one toolkit.

Requirements
------------

Require to install gnu-tar in macOS, use `brew install gnu-tar` to install.

Role Variables
--------------

List of variables in ansible-role-bun:

```sh
---
bun_repo_base: "https://api.github.com/repos/oven-sh/bun/releases/"
bun_version: "latest"
bun_git_token: ""
bun_retry_on_failure: 5
bun_arch_type:
  - { key: "aarch64", value: "aarch64" }
  - { key: "x86_64", value: "x64" }
  - { key: "arm64", value: "aarch64" }

# to determine multi version or single version installation
bun_multi_version: false
# force to set bun binary as default globally on multi version installation
bun_multi_set_default: false
```


Dependencies
------------

None.

Example Playbook
----------------

```sh
- hosts: servers
  roles:
    - devetek.bun
```

Todo
-------
- [ ] Support local user or global installation


License
-------

MIT

Author Information
------------------

[Nedya Prakasa]. Role created for [dPanel].

[dPanel]: https://cloud.terpusat.com/
[Nedya Prakasa]: https://github.com/prakasa1904
[mit]: https://opensource.org/licenses/MIT
[Bun]: https://bun.sh/
[devetek]: https://github.com/devetek