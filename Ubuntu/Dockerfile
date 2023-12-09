FROM ubuntu:latest

LABEL authors="Jonatan Huergo"

ENV TZ=Asia/Manila
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone


RUN apt-get update && \
    apt-get install -y apache2 && \
    apt-get install -y php libapache2-mod-php && \
    rm -rf /var/lib/apt/lists/*

# Remove the default Apache index.html file
RUN rm -rf /var/www/html/*

# Copy your PHP application into the container
COPY ./App/index.php /var/www/html/

# Enable the Apache rewrite module
RUN a2enmod rewrite

# Set ServerName to suppress warning messages
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf

# Expose port 80 for the web server
EXPOSE 80

# Start Apache in the foreground
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]