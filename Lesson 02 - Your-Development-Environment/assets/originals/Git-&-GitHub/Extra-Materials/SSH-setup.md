#### Generating an SSH Key

Start by opening up your terminal and checking for existing keys.
```bash
$ ls -al ~/.ssh
#Lists the files in your .ssh directory, if they exist
```
If you see two files: `id_rsa` and `id_rsa.pub`, skip to **[SSH Agent](#ssh_agent)**. Otherwise generate an SSH key.

#### SSH Key Creation
```bash
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
#Creates a new ssh key, using the provided email as a label
#Generating public/private rsa key pair.
```
_Include the double-quotes around your email address._


You will be prompted by the terminal for a default location to save the SSH key.
```bash
Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
```
_Make sure the default location is within your user profile.  Setting it in the root or another user profile **will** cause issues._  


Now, you will be prompted for a passphrase and then prompted to re-enter it. (This part is not necessary)
```bash
Enter new passphrase (empty for no passphrase): [Type new passphrase]
Enter same passphrase again: [One more time for verification]
```

The terminal should provide you your ssh key's fingerprint and random art image. 

**Note:** The first time you use your key, you will be prompted to enter your passphrase. If you choose to save the passphrase with your keychain, you won't have to enter it again.

<a name="ssh_agent"></a>
#### SSH Agent

Start the ssh-agent in the background.   

```bash
$ eval "$(ssh-agent -s)"
```
The SSH Agent is a background program that manages our SSH keys. Once we add our password to the SSH Agent, we will never be prompted for the same password again.  

If you're using macOS Sierra 10.12.2 or later, you will need to modify your ~/.ssh/config file to automatically load keys into the ssh-agent and store passphrases in your keychain.

Check `.ssh` directory for `config` file.
```bash
$ ls ~/.ssh
```

You should see
- `config`  
- `id_rsa`	
- `id_rsa.pub`	  
- `known_hosts`

If you do not have the `config` file, create one using `touch`.
```bash
$ cd ~/.ssh
$ touch config
```
_Be sure to create the `config` file in the `.ssh` directory_


Using Finder GUI, navigate to your Home directory and find the .ssh folder.
_This is a hidden file.  You can use [This Guide](http://ianlunn.co.uk/articles/quickly-showhide-hidden-files-mac-os-x-mavericks/) to set your defaults to show hidden files._

Locate the `config` file within the `.ssh` folder and open it with your text editor of choice.  Add the following block of code to the file, save and close it.
```
Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa
```

This will allow the `config` file to automatically load keys into the ssh-agent as well as store passphrases in the keychain.

#### Add SSH private key to the ssh agent

```bash
$ ssh-add -K ~/.ssh/id_rsa
```

Our client side is all set up, now to configure the server side (GitHub).

#### Configure SSH in GitHub

Copy the ssh key to your clipboard, you can either do this manually by opening the `id_rsa.pub` file **or** use the below command in terminal.

```bash
$ pbcopy < ~/.ssh/id_rsa.pub
```
**Note:** `pbcopy` s a Mac only command.

On your GitHub profile, navigate over to **Settings** in the top right corner and select **SSH and GPG keys** from the sidebar.

Click **New SSH Key**

Add an appropraite title for the key.  Remember, this key is associated with a specific user profile on a specific machine, so having a title referencing either or both of those aspects would be beneficial. 

Paste the key into the "Key" field and click **Add SSH Key**.  You may be prompted for your _Github_ password.

#### Check Connection

Before we get too excited, lets check to make sure everything is working.

In terminal enter
```bash
$ ssh -T git@github.com
#Attempts to ssh to GitHub
```

You may see an authenticity message like below.
```bash
The authenticity of host 'github.com (207.97.227.239)' can't be established.
#RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
#Are you sure you want to continue connecting (yes/no)?
```

Verify that the fingerprint prompted is one of the [keys provided by GitHub](https://help.github.com/articles/github-s-ssh-key-fingerprints/) before typeing 'yes'.


If all goes according to plan you should see a similar output to this:
```bash
Hi <username>! You've successfully authenticated, but GitHub does not
#provide shell access.
```

**Congratulations** on creating your own, and possibly first, security layer!  

Now, you can use the SSH option to clone any repo that exists on your GitHub account to your local machine.  Additionally, the secure tunnel will be used for all pushes and pulls from your GitHub to your local Machine.

Note: You will need to complete this process twice.  Once for your GitHub account and once for your GitHub Enterprise account.    
Note: Setting up the SSH agent is **critical** if you don't want to be prompted for a password everytime you push or pull.

#### Additional SSH Troubleshooting:

**Access Denied**  
If you receive a message about "access denied," please notify an instructor or you can read [these instructions for diagnosing the issue.](https://help.github.com/articles/error-permission-denied-publickey/)

**HTTPS to SSH switch**  
If you're switching from HTTPS to SSH, you'll now need to update your remote repository URLs. For more information, see [Changing a remote's URL.](https://help.github.com/articles/changing-a-remote-s-url/)
