FROM node:16

# Install Grunt
RUN npm install -g grunt-cli bower && \
	npm cache clean --force

# Install OpenJDK 11 JRE
RUN apt-get update && \
	apt-get install -y openjdk-11-jre \
	; \
	rm -rf /var/lib/apt/lists/*;

USER node
WORKDIR /home/node/app

# Create node_modules and lib folders to prevent permission
# issues when mounting volumes from the dev container
RUN mkdir node_modules && \
	mkdir lib
