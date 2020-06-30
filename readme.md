# Let's encrypt helper scripts

Let's encrypt SSL certificates can be requested by only 2 parameters: email address and domain list.

## Prerequsites

- Docker
- Route53 credentials from AWS

## Route53 credentials setup

The aws credentials are expected to be in this location: ~/.aws/certbot

Example ~/.aws/certbot 

    [default]
    aws_access_key_id = ACCESS_KEY_ID
    aws_secret_access_key = SECRET_ACCESS_KEY

## Create wildcard certificates

    ./create_certs jane@example.com "*.mydomain.com,mydomain.com"

## renew certificates

    ./renew_certs
