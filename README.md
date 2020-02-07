# Role Name

[![Build Status][travis-badge]][travis-link]
[![Galaxy Role][role-badge]][galaxy-link]
[![GPLv3 licensed][gpl-badge]][gpl-link]

Ansible role to route all system notification to a Telegram bot.

![tgnotify][demo]

## Requirements

* Telegram account
* Telegram bot token
* Telegram bot chat_id

Follow this great post to get start with [BotFather][BotFather].

## Role Variables

A description of the settable and notable variables for this role are listed below,
including any variables that are in [defaults/main.yml](defaults/main.yml),
[vars/main.yml](vars/main.yml), and any variables that can/should be set via
parameters to the role.

```yaml
postfix_tg_bot_token: "bot123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11"
```

Telegram bot token.

```yaml
postfix_tg_chat_id: "246367260"
```

Notifications will be forwarded to the Telegram chat represented by chat_id.

Any other variables not referenced above have sane defaults and are self
explanatory.

## Dependencies

None.

## Example Playbook

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  vars:
    postfix_tg_bot_token: "bot123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11"
    postfix_tg_chat_id: "246367260"
  roles:
     - { role: hurricanehrndz.tgnotify }
```

## License

[GPLv3][gpl-link]

## Author Information

Carlos Hernandez | [e-mail](mailto:hurricanehrndz@techbyte.ca)

[BotFather]: https://tutorials.botsfloor.com/creating-a-bot-using-the-telegram-bot-api-5d3caed3266d
[gpl-badge]: https://img.shields.io/badge/License-GPLv3-blue.svg?style=for-the-badge
[gpl-link]: https://raw.githubusercontent.com/hurricanehrndz/ansible-tgnotify/master/LICENSE
[travis-badge]: https://img.shields.io/travis/hurricanehrndz/ansible-tgnotify/master.svg?style=for-the-badge&logo=travis
[travis-link]: https://travis-ci.org/hurricanehrndz/ansible-tgnotify
[galaxy-link]: https://galaxy.ansible.com/hurricanehrndz/ansible-tgnotify/
[role-badge]: https://img.shields.io/ansible/role/d/45889?style=for-the-badge
[demo]: ./images/demo.gif
