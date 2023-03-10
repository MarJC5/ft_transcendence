FROM nginx:1.23-alpine

# Install dependencies
RUN apk update && apk upgrade \
    && apk add --no-cache --quiet --update \
    	  openssl certbot vim curl bash zsh git gettext

RUN chown -R nginx:nginx /usr/share/nginx/html && \
    chmod -R 755 /usr/share/nginx/html

# Expose the port the Nginx server will be running on
EXPOSE 443

# Start the Nginx server
CMD ["nginx", "-g", "daemon off;"]
