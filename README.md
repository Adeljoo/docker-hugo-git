# docker-hugo-git

Dockerfile with hugo, git and nginx that updates via git push

## Getting started
* Git clone this repository
* Create the directories `html`, `repos` and `keys`
* Copy the public ssh key from your pc / laptop into the `keys` folder
* Fill out all variables in the `.env` file
* Copy a bare clone of your repository into the `repos` folder
* Copy the file `post-receive.tmpl` into the your repo folder as `hooks/post-receive`, replace the YOURREPO placeholder and make it executable.
* The push/pull url is: ssh://git@yourdomain.de:yourport/git-server/repos/yourrepository (replace yourdomain, yourport and yourrepository)
