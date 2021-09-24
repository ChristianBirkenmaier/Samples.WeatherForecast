Source code from https://dev.to/newday-technology/api-s-from-dev-to-production-428i

Build the container with
docker build -t samples.weatherforecast:v2 .

Compare the size of the new image to the size of the old from part 1
docker image ls
Notice how it is significantly smaller

Now run it with
docker run -it --rm -p 8080:80 samples-weatherforecast:v2

You can check for data with eg Postman on http://localhost:8080/weatherforecast
