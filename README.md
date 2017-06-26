# docker-hugo-git

Dockerfile with hugo, git and nginx that updates via git push

## Getting started
* Git clone this repository
* Create the directories `html`, `repos` and `keys`
* Copy the public ssh key from your pc / laptop into the `keys` folder
* Create a `.env` file and insert the following contents

```
CONTAINER_NAME=yourcontainer
URL=yourdomain.de
GIT_PORT=2222
```

* Copy a bare clone of your repository into the `repos` folder and rename it to `repo.git`
* Copy the file `post-receive.tmpl` into the your repo folder as `hooks/post-receive`, replace the YOURREPO placeholder and make it executable.
* The push/pull url is: ssh://git@yourdomain.de:yourport/git-server/repos/repo.git
