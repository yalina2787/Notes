# Create an GPG key

##Open terminal
1. Install Homebrew 
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
2. Check whether it is installed successfully or not. 
```
brew help
```
3. Install GPG
```
brew install gnupg
```
4. Check GPG version
```
gpg --version
```
5. 
If you are on version 2.1.17 or greater, paste the text below to generate a GPG key pair.
```
gpg --full-generate-key
```
6. Please select what kind of key you want:
Recommended by Github, press ```enter``` to select default.
7. Please select which elliptic curve you want:
Recommended by Github, press ```enter``` to select default.
8. Please specify how long the key should be valid.
Recommended by Github, press ```0``` to select Key does not expire at all.
9. Is this correct? ```y```
10. GnuPG needs to construct a user ID to identify your key.
Enter your user name
11. Email address, use your GitHub-provided no-reply email address
To find the no-reply email address: github setting => email => fing the your no-reply email address with @users.noreply.github.com .
12. comment: any comment you want to enter
13. You selected USER_ID?
Check whether anything need to be changed, if everything is correct for you, press ```o``` (okay) to continue.
14. please enter the passphrase
Setting your GPG key password.
15. Get your GPG key ID.
    
```gpg --list-secret-keys --keyid-format=long```
[keyboxd]
------ sec   ..../xxxxxxxxxxxxxxxx date  [SC] , xxxxxxxxxxxxxxxx is your GPG key ID
17. Export the GPG key ID xxxxxxxxxxxxxxxx in ASCII armor format, substituting in the GPG key ID xxxxxxxxxxxxxxxx with your GPG key ID.
```gpg --armor --export xxxxxxxxxxxxxxxx```
18. Add new GPG key in github profile
Github setting => SSH keys and GPG keys => new GPG key, paste your exported armor format form the step 16.

-----BEGIN PGP PUBLIC KEY BLOCK----- your armor format GPG key ID -----END PGP PUBLIC KEY BLOCK-----.



