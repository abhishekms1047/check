FROM selenium/standalone-chrome-debug:3.141.59-antimony
USER root
RUN apt-get update -qq && apt-get install nginx --no-install-recommends -y
COPY ./nginx.conf /etc/nginx/sites-available/check-api
RUN rm /etc/nginx/sites-enabled/default
COPY ./entry_point.sh /
RUN chmod +x /entry_point.sh
CMD ["/entry_point.sh"]
