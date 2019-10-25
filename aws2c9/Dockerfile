FROM alpine/git AS git
WORKDIR /app
RUN git clone https://github.com/secobau/4543

FROM nginx:stable-alpine AS utils
RUN apk add apache2-utils
RUN htpasswd -b -c htpasswd user password

FROM nginx:stable-alpine
WORKDIR /etc/nginx/conf.d/
RUN rm -f *
COPY --from=git /app/4543/aws2c9/aws2c9.conf .
COPY --from=utils htpasswd .
