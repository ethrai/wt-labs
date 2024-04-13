FROM nginx:alpine
WORKDIR /app
COPY app  .
COPY ./nginx.conf /etc/nginx/nginx.conf

# Add node and CSS preprocessor
RUN apk add --update --no-cache nodejs npm
RUN npm install -g sass

# Compile scss to css
RUN sass /app/static/styles.scss /app/static/styles.css