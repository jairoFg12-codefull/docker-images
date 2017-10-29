FROM node:6.9
MAINTAINER jairoFg12
LABEL authors="Jairo Fdez <jairog12@outlook.com>"

# prepare a user which runs everything locally! - required in child images!
RUN useradd --user-group --create-home --shell /bin/false app

## Extras for protactor ejejmop
# RUN curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
#     && sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list' \
#     && apt-get update && apt-get install -y Xvfb google-chrome-stable \
#     && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# ADD xvfb.sh /etc/init.d/xvfb 
# ADD entrypoint.sh /entrypoint.sh

# ENV DISPLAY :99.0
# ENV CHROME_BIN /usr/bin/google-chrome

# RUN chmod +x /etc/init.d/xvfb \
#     && chmod +x /entrypoint.sh
# ## Extras for protactor

ENV HOME=/usr/src/app
RUN mkdir $HOME
WORKDIR $HOME

RUN npm install -g @angular/cli && npm install -g angular-cli-ghpages && npm cache clean

EXPOSE 4200
EXPOSE 49153
EXPOSE 9876
# e2e
EXPOSE 49152 

#ENTRYPOINT ["/entrypoint.sh"]
ENTRYPOINT ["bash"]
