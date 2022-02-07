FROM nginx:stable-alpine
COPY nginx/conf.d/default.conf /etc/nginx/templates/default.conf.template
RUN rm -rf /usr/share/nginx/html/*
COPY ./dist /usr/share/nginx/html
CMD ["nginx", "-g", "daemon off;"]
