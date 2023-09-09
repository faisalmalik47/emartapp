FROM node:14 AS nodeapi-build 
WORKDIR /usr/src/app
COPY . ./nodeapi
RUN npm install

FROM node:14
WORKDIR /usr/src/app/
COPY --from=nodeapi-build /usr/src/app/nodeapi/ ./
RUN ls
EXPOSE 5000
CMD ["npm", "start"]
