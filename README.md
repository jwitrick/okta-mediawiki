# okta-mediawiki

# okta-simplesamlphp

## Overview
This Docker image contains an installation of SimpleSAMLphp (based upon Unicon/simplesamlphp) and is customized to authentication against Okta.

## Using the Image
This image requires 2 environment variable to fully function:

* SIMPLESAML_PATH
* BASE_URL
* OKTA_METADATA_URL

### Docker Compose
This repository comes with a compose stack file 'stack.yml'.

If you update the values in the stack.yml with the proper values, then the image can be launched by:

`docker-compose -f stack.yml up`

### Manual Docker
Another way to use the image is:

`docker run -p 9000:80 -e SIMPLESAML_PATH=/simplesaml/ -e BASE_URL=http://localhost:9000 -e OKTA_METADATA_URL=<URL_FROM_OKTA> okta-simplesamlphp `

# okta-mediawiki