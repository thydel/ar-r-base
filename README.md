# Role Name

Install r-base from cran.r-project.org

## Role Variables

As told by [DEBIAN PACKAGES OF R SOFTWARE](http://cran.r-project.org/bin/linux/debian/README.html) on cran.r-project.org

```yaml
rbase_keyserver: keys.gnupg.net
rbase_id: 381BA480
rbase_repo: deb http://cran.rstudio.com/bin/linux/debian wheezy-cran3/
https_proxy: # use to set environment https_proxy, default(omit)
```

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: thydel.r-base
      http_proxy: http://my.proxy.tld:3128
```

## Usage

ansible-playbook -i server, r-base-play.yml --check

## License

MIT

