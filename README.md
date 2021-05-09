s3cmd-role
=========

[![CI](https://github.com/dtoch56/ansible-role-s3cmd/workflows/CI/badge.svg?event=push)](https://github.com/dtoch56/ansible-role-s3cmd/actions?query=workflow%3ACI)


s3cmd configuration

[Amazon S3 Tools: Command Line S3 Client Software and S3 Backup](https://s3tools.org/s3cmd)

[s2cmd GitHub page](https://github.com/s3tools/s3cmd)

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

| Variable                      | Description                          | Default                                                  |
| ----------------------------- |:------------------------------------ |:-------------------------------------------------------- |
| s3cmd_access_key              | S3 access key                        |                                                          |
| s3cmd_access_token            | S3 access token                      |                                                          |
| s3cmd_secret_key              | S3 secret key                        |                                                          |
| s3cmd_location                | Bucket location                      | US                                                       | 
| s3cmd_host_base               |                                      | s3.amazonaws.com                                         | 
| s3cmd_host_bucket             |                                      | %(bucket)s.s3.amazonaws.com                              | 
| s3cmd_cloudfront_host         |                                      | cloudfront.amazonaws.com                                 | 
| s3cmd_multipart_chunk_size_mb |                                      | 15                                                       | 
| s3cmd_multipart_max_chunks    |                                      | 10000                                                    |
| s3cmd_recv_chunk              |                                      | 65536                                                    |
| s3cmd_send_chunk              |                                      | 65536                                                    |
| s3cmd_simpledb_host           |                                      | sdb.amazonaws.com                                        |
| s3cmd_socket_timeout          |                                      | 300                                                      |
| s3cmd_throttle_max            |                                      | 100                                                      |
| s3cmd_website_endpoint        |                                      | http://%(bucket)s.s3-website-%(location)s.amazonaws.com/ |
| s3cmd_website_index           |                                      | index.html                                               |


Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: dtoch56.s3cmd }

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2021 by DToch.

Development
------------------

    pip install pipenv
    pipenv install
