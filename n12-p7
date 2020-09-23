FROM openjdk:11.0.8-jre-slim
RUN apt-get update
# Install gnupg
RUN apt-get -y install curl gnupg
# Install nodejs
RUN curl -sL https://deb.nodesource.com/setup_12.x  | bash
RUN apt-get install --yes nodejs
# Install git
RUN apt-get install -y git
# Install Chrome
RUN set -xe \
&& curl -fsSL https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
&& echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" > /etc/apt/sources.list.d/google-chrome.list \
&& apt-get update \
&& apt-get install -y google-chrome-stable \
&& rm -rf /var/lib/apt/lists/*
# Install Protractor
RUN npm install -g protractor@7.0.0
