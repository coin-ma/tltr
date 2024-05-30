## multiple github account
* ssh-keygen -t rsa -b 4096 -C "your_email_account1@example.com"
* add key to ssh-agent
  ```
  eval "$(ssh-agent -s)"
  ssh-add ~/.ssh/id_ma
  ssh-add ~/.ssh/id_rsa_account2
  ```

* config file
  ```
  
Host github-ma
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ma

Host github-nicecord
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_nicecord

  ```

* use custom host

git clone git@github-ma:{accountname}/repository.git
