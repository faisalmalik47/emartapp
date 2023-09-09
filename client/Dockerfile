FROM node:14 AS WEB-BUILD
WORKDIR /client/
COPY . .
RUN  npm install && npm run build --prod


FROM nginx
COPY --from=WEB-BUILD client/dist/client/  /usr/share/nginx/html

COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 4200