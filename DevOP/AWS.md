
# EC2 for git server

download the name.pem file
run the code and ssh inside the server
```
ssh -i "git.pem" ubuntu@ec2-13-232-166-162.ap-south-1.compute.amazonaws.com
```

```
sudo add user git 
sudo su git
```

dont know the password to ubuntu machine use 'crtl'+d

```
// after going back to ubuntu
sudo chown -R git /var/lib/git
```

create a dot git file 
```
mkdir my-review-app.git
cd my-review-app.git

git init --bare
```
add your own ssh key to the t2.micro
```

```
```
#this will show 
cat ~/.ssh/id_ed25519.pub 
```

clone the repo u made inside the t2.micro
```
git clone git@13.232.166.162:/var/lib/git/my-review-app.git
```