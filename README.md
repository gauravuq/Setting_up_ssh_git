# Setting_up_ssh_git
 
1. ssh-keygen -t ed25519 -C "your_email@example.com" -- generate the ssh private and public key files in your ssh folder
2. activate the ssh agent -- **eval ssh-agent -s**.
    * **ssh-add -l** -- to check if there is any key in the agent or not.
3. Sample private key added to ssh agent -- **ssh-add ~/.ssh/[private key file name]**.
    * For windows we need to start the OpenSSH Authentication agent. 
      * Then do **ssh-add [private key file name]**
4. Add the public key to your github account.
    * **clip < ~/.ssh/[public key file name]**
5. Test if your stuff is working
    * **ssh -T git@github.com** .