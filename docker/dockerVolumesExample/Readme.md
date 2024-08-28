docker build -t write-date-image .

docker run --rm -v $(pwd)/output:/output write-date-image



rm -rf output 
