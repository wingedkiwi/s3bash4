# s3-bash4

_s3-bash4_ is a small collection of _Bash_ scripts to do simple interaction with _Amazon S3_ using [_AWS Signature Version 4_](http://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html). The advantage of using _s3-bash4_ is that it's extremely lightweight and easy to use. No need to setup _Python_, _Java_, _Ruby_ and co.

This is inspired by the discontinued [_s3-bash_](https://github.com/cosmin/s3-bash) from _cosmin_. I was in need of a _Bash_ version that supports the newer _AWS Signature Version 4_.

## Usage

```sh
  # Get file from bucket:
  s3-get -k {accesskey} -s /{path}/{secretid} -r {region} [-d {customdomain}] /{bucketname}/{filename} > {filename}

  # Upload file to bucket:
  s3-put -k {accesskey} -s /{path}/{secretid} -r {region} [-d {customdomain}] -T /{path}/{filename} /{bucketname}/{filename}

  # Delete from bucket:
  s3-delete -k {accesskey} -s /{path}/{secretid} -r {region} [-d {customdomain}] /{bucketname}/{filename}
```

## Environment Variables

Variable               | Description
---------------------- | -----------------------------------------------------------
`AWS_ACCESS_KEY_ID`    | Default _AWS Access Key ID_
`AWS_SECRET_ACCESS_KEY`| Default _AWS Secret Access Key_
`AWS_DEFAULT_REGION`   | Default _AWS S3 Region_
`S3_DEFAULT_DOMAIN`    | Default _S3 custom domain_
`AWS_SECURITY_TOKEN`   | Default _AWS Security Token for temporary credentials_

## Requirements

- _GNU Bash_
- _OpenSSL_
- _cUrl_

## License

This work is released under the _Apache License Version 2.0_
