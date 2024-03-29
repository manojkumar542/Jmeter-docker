# Jmeter Docker image with all plugins installed
Apache JMeter : an application designed to load test functional behavior and measure performance - https://jmeter.apache.org

JMeter Plugins : an independent set of plugins - https://jmeter-plugins.org

The version number is composed of two version numbers
the first is the version of the Apache JMeter embedded in this docker image
the second is for this docker image itself

Update the variables accordingly for your requirement

# Build and Run docker jmeter images as below
docker build -t tag any name .

ex: docker build -t jmeter-docker:latest .

docker run -it --name any name image name

ex: docker run -it --name jmeterimage jmeter-docker:latest
# To store the results into your local machine use volumes as below

docker run -it --name any name -v hostfolder:containerfolder image name
  
# ex: docker run -it --name jmeterimage -v ${pwd}/output:/results jmeter-docker:latest


For more details follow my blogs
* https://sreinsights.wordpress.com/2021/01/22/easy-setup-to-dockerize-jmeter-monitoring-solution/
* https://sreinsights.wordpress.com/2020/09/11/run-jmeter-in-docker-and-save-results-in-csv/
* https://sreinsights.wordpress.com/2020/02/01/setup-jmeter-in-linux-docker-container-with-all-plugins/
