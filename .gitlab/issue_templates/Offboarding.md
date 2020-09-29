<!--
This template should be used for offboarding Arch Linux team members.
-->

# Offboarding an Arch Linux team member

## Details

- **Team member username**:
- **Currently held roles**: <!-- Add known roles here like TU, DevOps, etc -->

## All roles checklist

- [ ] Remove user email by reverting instructions from `docs/email.md`.
- [ ] Set user to inactive in archweb: https://www.archlinux.org/admin/auth/user/

## TU/Developer offboarding checklist

- [ ] Remove entry in `group_vars/all/archusers.yml`.
- [ ] Remove SSH pubkey from `pubkeys/<username>.pub`.
- [ ] Run `ansible-playbook -t archusers playbooks/*.yml`.
- [ ] Remove the user from the `Trusted Users`/`Developers` groups on Keycloak.
- [ ] Moderate email address on [arch-dev-public](https://lists.archlinux.org/admin/arch-dev-public/members) (find member and moderate)
- [ ] Remove member from [arch-tu mailing lists](https://lists.archlinux.org/admin/arch-tu/members)
- [ ] Remove member from [staff mailing lists](https://lists.archlinux.org/admin/staff/members)
- [ ] Remove member from [arch-dev mailing lists](https://lists.archlinux.org/admin/arch-dev/members)

## DevOps offboarding checklist

- [ ] Remove entries in `group_vars/all/root_access.yml`.
- [ ] Run `ansible-playbook -t root_ssh playbooks/*.yml`.
- [ ] Run `ansible-playbook playbooks/hetzner_storagebox.yml playbooks/rsync.net.yml`.
- [ ] Remove the user from the `DevOps` group on Keycloak.
- [ ] Remove member from [arch-dev mailing lists](https://lists.archlinux.org/admin/arch-devops-private/members)
