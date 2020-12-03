#Exercise steps

1. Create a `my-apache` directory (our context build)
1. Move into `my-apache` directory
1. Create a basic html file, called index.html

```   
<!DOCTYPE html>
<html>
<body>

    <h1>Running in my Docker container</h1>
    <p>This is my web page running inside my Docker container</p>

</body>
</html>
```
 
1. Create a Docker file with the following specifications:
   1. Use apache(httpd) as the base image
   1. The version of the base image is `2.4.46`
   1. Copy the index.html file to the Docker image, in /var/www/html/
   1. Execute the /usr/sbin/httpd command, with the "-D FOREGROUND" option
1. Build the image using the `docker build` command, and tag the image as my-apache-image, version 1.0.0
1. List the images and ensure that your image is displayed
1. Run the image as a container and publish the 80 container port in 8080 host port. 
1. Visit the url `http://localhost:8080` u¿in your web browser.

