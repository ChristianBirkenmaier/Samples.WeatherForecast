Source code from https://dev.to/newday-technology/api-s-from-dev-to-production-428i

Build the container with
docker build -t samples-weatherforecast:latest .

Now run it with
docker run -it --rm -p 8080:80 samples-weatherforecast:latest

You can check for data with eg Postman on http://localhost:8080/weatherforecast
