<!--
This template should be used for onboarding new Arch Linux team members.
It can also be used as a reference for adding new roles to an existing team member.
-->

# Onboarding an Arch Linux team member

## Details

- **Team member username**:

## All roles checklist

- [ ] Add new user email as per `docs/email.md`.
- [ ] Create a new user in archweb: https://www.archlinux.org/devel/newuser/
      This is also linked in the django admin backend at the top
- [ ] Subscribe user to internal [staff mailing list](https://lists.archlinux.org/admin/staff/members/add)

## Developer onboarding checklist

- [ ] Add entry in `group_vars/all/archusers.yml`.
- [ ] Add SSH pubkey to `pubkeys/<username>.pub`.
- [ ] Run `ansible-playbook -t archusers playbooks/*.yml`.
- [ ] Assign the user to the `Developers` groups on Keycloak.
- [ ] Subscribe user to internal [arch developer mailing list](https://lists.archlinux.org/admin/arch-dev/members/add)
- [ ] Whitelist email address on [arch-dev-public](https://lists.archlinux.org/admin/arch-dev-public/members) (find member and unmoderate)

## TU onboarding checklist

- [ ] Add entry in `group_vars/all/archusers.yml`.
- [ ] Add SSH pubkey to `pubkeys/<username>.pub`.
- [ ] Run `ansible-playbook -t archusers playbooks/*.yml`.
- [ ] Assign the user to the `Trusted Users` groups on Keycloak.
- [ ] Whitelist email address on [arch-dev-public](https://lists.archlinux.org/admin/arch-dev-public/members) (find member and unmoderate)
- [ ] Subscribe user to internal [trusted user mailing list](https://lists.archlinux.org/admin/arch-tu/members/add)

## DevOps onboarding checklist

- [ ] Add entries in `group_vars/all/root_access.yml`.
- [ ] Run `ansible-playbook -t root_ssh playbooks/*.yml`.
- [ ] Run `ansible-playbook playbooks/hetzner_storagebox.yml playbooks/rsync.net.yml`.
- [ ] Assign the user to the `DevOps` group on Keycloak.
- [ ] Subscribe user to [arch-devops-private mailing lists](https://lists.archlinux.org/admin/arch-devops-private/members/add)

## Wiki Administrator checklist

- [ ] Assign the user to the `Wiki Admins` group on Keycloak.
