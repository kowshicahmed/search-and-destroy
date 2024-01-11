# Create venv
	apt install python3.8-venv						# install venv creation
	sudo python3 -m venv .venv						# create a virtual env
	source .venv/bin/activate						# activate the virtual env
	pip install -r python_datascience.txt			# install packages in virtual env with requirements file
	sudo rm -rf venv								# remote venv after deleting
	python -m ipykernel install --user --name=myenv	# install jupyter kernel for venv

**for vscode -> ctl + shift + p then add the venv**

# Rebuild python
	sudo apt-get update
	sudo apt-get install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev
	wget https://www.python.org/ftp/python/3.9.7/Python-3.9.7.tgz
	tar -xzvf Python-3.9.7.tgz
	cd Python-3.9.7
	./configure --enable-optimizations
	make
	sudo make install
	python3 --version
	cd ..
	rm -r Python-3.9.7
	rm Python-3.9.7.tgz