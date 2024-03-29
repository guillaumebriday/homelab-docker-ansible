# Ansible playbook for my Home Media Server

This is an [Ansible](https://www.ansible.com) playbook to install and configure some apps on my Synology NAS with [Docker](https://www.docker.com).

## Requirements

+ Ansible >= 2.4.0.

## Applications

This playbook is designed to install a bunch of useful apps :

+ [Tautulli](https://tautulli.com/)
+ [Watchtower](https://github.com/containrrr/watchtower/)
+ [Youtube-dl-server](https://github.com/manbearwiz/youtube-dl-server)
+ [Pi-hole](https://pi-hole.net/)

## Installing on production

Copy the hosts example file and change the values to your needs :

```bash
$ cp hosts.ini.example hosts.ini
```

Then run the playbook :

```bash
$ ansible-playbook -i hosts.ini playbook.yml
```

If you want to run the playbook locally, set the address in the hosts file:
```ini
[webservers]
localhost ansible_connection=local
```

## Contributing

Do not hesitate to contribute to the project by adapting or adding features ! Bug reports or pull requests are welcome.

## License

This project is released under the [MIT](http://opensource.org/licenses/MIT) license.
