# To change user name and email

```
    git config --global user.name "ashwin"
    git config --global user.email ashwin@mail.com
```

- project - The data is stored directly in the corresponding project(repository) under .git/config.
- global - for all repositories of the current user. The config file can be found in your home directory ~/.gitconfig.
- system - This is a system wide configuration and is available for all users and all repositories. You will find it in /etc/gitconfig.

# list user details for repo

```
git config --list
git config --global --get user.name
git config --global --get user.email

git config --get user.name
git config --get user.email
```

# Adding remote url

```
    git remote add origin <remote url>
```

# Updating remote url

```
    git remote set-url origin <remote url>
```

# Amend to previous commit

- Amend to commit with comment

```
    git commit --amend -m <commit message>

```

- Amend without message

```
    git commit --amend --no-edit

```

# Merge conflicts resolve

- theirs - Accept incoming change.
- ours - Accept outgoing change.

```
    git pull -X theirs (for accepting incoming change)
    git checkout --theirs path/to/file(already conflicted state)
    git checkout --theirs .
    git checkout --ours .


```
