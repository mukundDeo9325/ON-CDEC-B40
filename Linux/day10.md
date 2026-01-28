### password and User management and Group 
# Linux Password & Group Management

## Using passwd Command

Change password:
```bash
passwd username
```

Lock user:
```bash
passwd -l username
```

Unlock user:
```bash
passwd -u username
```
---

## Account Locking & Expiration

```bash
chage -l username   ## Check current policy
chage -M 90 username    ## Set maximum password validity to 90 days
chage -E 2025-12-31 username    ## Set account expiry date ; After 31 Dec 2025, user cannot log in (even with correct password)
```

---

## Understanding /etc/shadow Fields

| Field | Description |
|----|---------|
| Username | Account name |
| Password | Encrypted password |
| Last change | Days since 1970 |
| Min | Min days |
| Max | Max days |
| Warn | Warning |
| Inactive | Inactive days |
| Expire | Expiry date |

---

## Using chage Command

```bash
chage username
```

---

## Introduction to Linux Groups

Groups are used to manage permissions for multiple users.

---

## Types of Groups

| Type | Description |
|----|-------------|
| Primary | Default group |
| Secondary | Additional groups |

---

## Creating & Deleting Groups

```bash
groupadd devops  ## New group create
groupdel devops   ## Existing group delete
```

---

## Modifying Groups

```bash
groupmod -n newgroup oldgroup  ## changing group name 
```

---

## Managing Group Membership

```bash
usermod -aG devops devuser
gpasswd -d devuser devops
```
- `usermod -aG` safely adds a user to a secondary group, while `gpasswd -d` removes a user from a group.
---

## Viewing Group Info

```bash
groups username
cat /etc/group
```
