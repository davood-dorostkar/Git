## Configuring Git

### Get

show current global user name

```bash
git config --global user.name
```

show current global user email

```bash
git config --global user.email
```

show repo-specific user name: just ommit the `--global`

### Set

set global user email

```bash
git config --global user.email "davood.dorostkar.ut@gmail.com"
```

set global user name

```bash
git config --global user.name "davood"
```

set repo-specific user name: just ommit the `--global`

### Config with Commit
set the user for the specific commit:
```bash
git commit --author='Davood Dororstkar <davood.dorostkar.ut@gmail.com>' -m 'fix: issue with controller'
```

### remove

other cases are the same

```bash
git config --global --unset user.name
```
