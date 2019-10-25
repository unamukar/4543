FROM alpine/git AS git
WORKDIR /app
RUN git clone https://github.com/secobau/4543

FROM nginx:stable-alpine
WORKDIR /etc/nginx/conf.d/
RUN rm -f *
COPY --from=git /app/4543/ec2aws/ec2aws.conf .
