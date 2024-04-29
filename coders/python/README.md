# Node, Python and Conda Notes

## Node and npm

Check your versions

	node -v
	npm -v


To installing node if the version commands find nothing:

[NPMjs.com](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) recommends installing a Node Version Manager like [nvm](https://github.com/nvm-sh/nvm) to avoid permission errors when you run npm packages globally.

Or [Install node/npm](https://nodejs.org/en/download) locally. The installer includes the Node.js package manager (npm) within it, so you won't need to install npm separately.

Or update to the latest stable version of NodeJS
<!-- https://askubuntu.com/questions/426750/how-can-i-update-my-nodejs-to-the-latest-version-->

	npm install -g n &&
	sudo n stable




## Python

Install the latest Python.

	brew install python

List all Python versions installed on your system.

	ls -l /usr/local/bin/python*

If an old version of python is still appearing as the current version,
check if you are running the pyenv python environment.

	pyenv --version

If so, upgrade your python versions in pyenv to 3.12 or later.

	pyenv install 3.12
	pyenv global 3.12


## Conda

You can try using a cmd to upgrade, but you may need to download.

	conda update -n base -c defaults conda

[Download Anaconda](https://www.anaconda.com/download)

## Docker

On a Mac, if the `docker` cmd is not recognized, add the path `$HOME/.docker/bin` in the config file corresponding to your command terminal instance:  In the **Users\\[username]** folder, edit one of these hidden files: .zshrc, .bash_profile, .bashrc or .profile.

If you're transitioning from an old instance of [Docker](https://www.docker.com/products/docker-desktop/), you may need to reinstall or do a Docker reboot.

<!--
Probably not needed:

Run if your version of conda won't update on your Mac. [source](https://stackoverflow.com/questions/75988022/conda-wont-update-on-macos)

	brew install python &&
	conda install -n base -c defaults 'conda>=24.3.0'

For the python install, you may also need to run:

	xcode-select --install

Type "python" followed by hitting tab key to see your python versions.

Make python3.12 (or a newer version) the main version on your system:

https://stackoverflow.com/questions/74343871/how-do-i-fix-my-python-version-showing-up-in-terminal

	# If you already have a python sym-link or binary file there, rename it
	sudo mv /usr/local/bin/python /usr/local/bin/python-

	# create sym-link to python3.11
	sudo ln -s `which python3.12` /usr/local/bin/python

	# check the version
	python --version
-->

<!--

After running brew install python

Says 3.12, but python --version returns 3.8.5

==> No broken dependents to reinstall!
==> Caveats
==> python@3.12
Python has been installed as
  /usr/local/bin/python3

Unversioned symlinks `python`, `python-config`, `pip` etc. pointing to
`python3`, `python3-config`, `pip3` etc., respectively, have been installed into
  /usr/local/opt/python@3.12/libexec/bin

See: https://docs.brew.sh/Homebrew-and-Python
==> pipx
zsh completions have been installed to:
  /usr/local/share/zsh/site-functions
==> postgresql@14
This formula has created a default database cluster with:
  initdb --locale=C -E UTF-8 /usr/local/var/postgresql@14
For more details, read:
  https://www.postgresql.org/docs/14/app-initdb.html

To start postgresql@14 now and restart at login:
  brew services start postgresql@14
Or, if you don't want/need a background service you can just run:
  /usr/local/opt/postgresql@14/bin/postgres -D /usr/local/var/postgresql@14
 -->
