# Prerequisites

Download and install:

Node.js: https://nodejs.org/en/download
Docker Desktop: https://nodejs.org/en/download (Requires setting up an account do download)
Postman: https://www.postman.com/downloads/ (Postman Web alternatively)


## Installation (Windows)

Install NPM:

```CMD
npm install -g npm
```

Newman: Follow this guide: https://hub.docker.com/r/postman/newman/ - Sections: *Using the docker image* and *Running local collection files*: 

#Postman Collection*

Copy the attached Postman collection into a folder and then open a terminal from that folder.

*Import the Postman collection to check the attached description in the Overview section

##Execution

```CMD
docker run -v "%cd%":/etc/newman -t postman/newman:latest run NASA_CAD_API_Test.postman_collection.json --insecure
```

--insecure param to bypass the certificate verification step (With a certain dose of trust, we can assume that we are testing a trusted API like NASA’s.).

## COMMENTS

Unfortunately I didn't attach any visual test report; for some reason I was unable to run newman-reporter-html and/or newman-reporter-htmlextra, so to save time I skipped this step. I kept getting the error:


```
Newman: could not find "htmlextra" reporter.
Ensure that the reporter is installed in the same directory as Newman.
Please install the reporter using npm.
```

I think it's because of an incompatible node. JS version. as those reporters are at least (according to documentation, Node.js 18.0.0 compatible, not sure about the newer versions).
I attached a screenshot instead from the Docker/Newman test collection run.


## END