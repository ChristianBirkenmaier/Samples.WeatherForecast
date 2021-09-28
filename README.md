Github url: https://github.com/ChristianBirkenmaier/Samples.WeatherForecast

Source code from https://dev.to/newday-technology/api-s-from-dev-to-production-428i

Build the container with
docker build -t samples.weatherforecast:v2 .

Compare the size of the new image to the size of the old from part 1
docker image ls
Notice how it is significantly smaller

Now run it with
docker run -it --rm -p 8080:80 samples-weatherforecast:v2

You can check for data with eg Postman on http://localhost:8080/weatherforecast

Part 4:

We've created a github action workflow to create a new docker image whenever there is a push to the master branch

A built image can be downloaded via
docker pull ghcr.io/christianbirkenmaier/samples.weatherforecast:8c132d88c42fd10f9fe7e8b7801605b39cc211d0
