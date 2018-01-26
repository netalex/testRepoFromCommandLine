# Appunti vari di studio 2018

---

# come creare un repo su github da command line

https://stackoverflow.com/a/10325316/2079428

```
curl -u 'USER' https://api.github.com/user/repos -d '{"name":"REPO"}'
```

```
curl -u 'netalex' https://api.github.com/user/repos -d '{"name":"testRepoFromCommandLine"}'
```

 Remember replace USER with your username and REPO with your repository/application name!
```
git remote add origin git@github.com:USER/REPO.git
```
doesnt' work:
```
$ git push
The authenticity of host 'github.com (192.30.253.112)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'github.com,192.30.253.112' (RSA) to the list of known hosts.
Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```
works better:
```
git remote add origin https://github.com/netalex/testRepoFromCommandLine.git
```
also:
```
git push origin master
```
