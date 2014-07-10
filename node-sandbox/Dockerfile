FROM 	ubuntu:14.04
RUN     sudo apt-get update
RUN 	sudo apt-get -y install nodejs npm
ADD     . /node-sandbox
RUN	cd /node-sandbox; npm install

EXPOSE 	7074
CMD	["nodejs", "/node-sandbox/index.js"]
