FROM node:18.9.1-alphine3.19
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
WORKDIR /opt/server
RUN chmode roboshop:roboshop /opt/server
USER roboshop
COPY package.json /opt/server
COPY server.js /opt/server
RUN npm install
CMD ["node" ,"server.js"]
