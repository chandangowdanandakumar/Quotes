FROM scratch
ADD alpine-minirootfs-3.11.12-x86_64.tar.gz  /
EXPOSE 4200
RUN apk add --update nodejs npm
WORKDIR /usr/src/app
COPY package.json .
RUN npm install
COPY . .
EXPOSE 4200
CMD /usr/src/app/node_modules/.bin/ng serve --host 0.0.0.0 --disableHostCheck

