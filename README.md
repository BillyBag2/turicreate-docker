# turicreate-docker

## Building image for the first time.
```
cd docker
docker build -t billybag2/turicreate:latest .
```
## Running image for the first time to create container.
```
docker run -it --name tc billybag2/turicreate
```
## Starting the created container ofter exiting. 
```
docker start -i tc
```

## Using container with a command.
The default command takes you to the venv. If you overide the command then include using the virtual ennv in the custom command.
```
cd /venv && source bin/activate && <my custom command>
```
 ## Using container without virtualenv
 To not enter the virtualenv start the container with the command
  ```bash```

# About Samples
## Image Classification
### Original Page
https://apple.github.io/turicreate/docs/userguide/image_classifier/
### Files are downloaded to the docker image when it is built
 * Page: https://www.microsoft.com/en-us/download/confirmation.aspx?id=54765
 * Direct: https://download.microsoft.com/download/3/E/1/3E1C3F21-ECDB-4869-8368-6DEBA77B919F/kagglecatsanddogs_3367a.zip
### Running example
If not in virtualenv...
```
cd /venv
source bin/activate
```
Once inside the vertualenv
```
cd samples/image-clasification/
./1_makefram.py
```
