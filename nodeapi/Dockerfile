FROM node:14 AS nodeapi-build 
WORKDIR /nodeapi/
COPY . . 
RUN npm install

FROM node:14
WORKDIR /usr/src/app/
COPY --from=nodeapi-build /nodeapi/ ./
RUN ls
EXPOSE 5000
CMD ["npm", "start"]
