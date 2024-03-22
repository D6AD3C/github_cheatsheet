# Common Use

## Pull from GITHUB remote

```
git clone https://github.com/GROUP_OR_USER_NAME/REPO_NAME.git
```

## Push to GITHUB remote

```
git add .
git commit -m "update"
git push -u origin main
```

## Remotes

```
git remote add GIT_REMOTE_NAME REMOTE_URL
```

if you name the remote "gitlab" or "github" it will error.

#Credentials

Git takes a lot of liberties in terms of credential storage, to clean this up:

### Windows Certificates
If you authenticate from any prompt git most likely will make a windows credential automatically
start > credentials manager > windows credentials > (look for something git related)

```text
git config --global credential.https://github.com.useHttpPath true
```
This command makes each unique repo visited at github have to uniquely authenticate 

you can preview git global config here:
C:\Users\USERNAME\.gitconfig

here's an example of what it should look like:

```text
[filter "lfs"]
	clean = git-lfs clean -- %f
	smudge = git-lfs smudge -- %f
	process = git-lfs filter-process
	required = true
[user]
	name = name_tbd
	email = email_tbd@email_provider_tbd.com
[credential "https://github.com"]
	useHttpPath = true
[credential "https://gitlab.com"]
	useHttpPath = true
```
