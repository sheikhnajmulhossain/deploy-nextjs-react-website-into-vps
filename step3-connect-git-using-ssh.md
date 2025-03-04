# Connecting git using ssh

1. Generate a new SSH key if you don’t have one (or want a fresh one):
`ssh-keygen -t ed25519 -C "your_email@example.com"`

2. just press enter to skill passphrase till ssh key is generated

3. Add your private key to the SSH agent
`eval "$(ssh-agent -s)" ssh-add ~/.ssh/id_ed25519`

4. Add the public key to your GitHub account
a. Copy the public key contents to your clipboard:
`cat ~/.ssh/id_ed25519.pub`

5. Add it to GitHub:
Log into your GitHub account.
Go to Settings → SSH and GPG keys → New SSH key.
Give it a title (like “MyServerKey” or “RootKey”), then paste the public key into the key field and click Add SSH key.

6. Verify that SSH is working
`ssh -T git@github.com`
If everything is set up correctly, you should see a message like:
`Hi username! You've successfully authenticated, but GitHub does not provide shell access.`

