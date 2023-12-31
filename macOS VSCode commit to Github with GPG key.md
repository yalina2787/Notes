
1. Open terminal 
2. Set your commit userName and email
  
```
git config --global user.name "yourFirstName yourLastName"
```
  
3. Set your commit userName
The email address could be your email address. To protect the privacy, you could also use the no-prely email address provide by Github. To find your no-reply email address, your profile => Github setting => Email => find your no-reply address with @users.noreply.github.com
  
```
git config --global user.email "your no-repley@users.noreply.github.com"
```
4. List the long form of the GPG keys. 
```
gpg --list-secret-keys --keyid-format=long
```
5. Set your primary GPG signing key in Git, substituting the GPG primary key ID xxxxxxxxxxxxxxxx with your GPG key ID

In the listed [keyboxd], line sec .../xxxxxxxxxxxxxxxx date [SC], xxxxxxxxxxxxxxxx is your GPG key ID.

```
git config --global user.signingkey xxxxxxxxxxxxxxxx
```
6. Configure Git to sign all commits by default
```
git config --global commit.gpgsign true
```
7. Install pinentry-mac. When submitting code change to Github, VSCode will use pinentry-mac to show a dialog and let you enter the password for the GPG key.
```
brew install pinentry-mac
```
```
echo "pinentry-program $(which pinentry-mac)" >> ~/.gnupg/gpg-agent.conf
```
```
killall gpg-agent
```


