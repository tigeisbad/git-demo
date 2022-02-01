# ACC Spring 2022 GitHub Workshop
## Setting up your GitHub account

1. Set up your SSH key in WSL2:
```sh
# you will be prompted to set up a password -- just spam enter and accept the defaults
ssh-keygen -t ed25519
```
2. Obtain your public key:
```sh
# this will print your public key to the terminal -- make sure it ends with .pub
cat ~/.ssh/id_ed25519.pub
```
3. Copy the printed key to your clipboard.
4. Add the SSH key to your GitHub account (click your account icon > `Settings` > `SSH and GPG keys` > `New SSH key` > paste into `Key` > `Add SSH key`)

## Contributing a pull request

1. Open an issue with your name as the title in this repository (`Issues` > `New issue`).
2. Fork this repository to create an identical repository under your account (click the `Fork` icon in the upper-right corner).
3. Check out your forked repo. Make sure you use the `ssh` protocol over `https`. If you use HTTPS, you won't be able to make changes on the remote.
```sh
# the name in the link will be different!

git clone git@github.com:nhwn/git-demo.git
```
4. Add a file named `<your name>.md`.
5. Put your opinion on cats vs. dogs in the file, then save it.
6. Commit the file with your name as the commit message.
```sh
# this adds the file to staging
git add nathan.md
# this sets your changes in stone
git commit -m "haha your funny message goes here"
```
7. Push your changes to your remote repository.
```sh
# `-u origin <branch name>` is only necessary if the branch doesn't exist remotely
git push
```
8. Open a pull request that mentions the issue you opened in #1. The PR should merge the main branch in your remote repository to the ACC repository.
Example body:
```
This PR contains the work that closes #1 (put the actual number of the issue -- GitHub will automatically close the issue when the PR is merged).
```
9. Wait for the PR to be merged. When it's merged, you should see your contributions show up in the GitHub UI.k