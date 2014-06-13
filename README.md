# EdX Import
A simple bash library that makes searching for, downloading, decrypting, and combining EdX Research Data easier.

### Required Packages
 - gpg
 - awscli (via pip; maybe apt?)
 - jq
 - python2 (tested on python 2.7)

### Before you start
There should be a valid GPG key passphrase in the following environment variables:
 EDX_GPG_PASSPHRASE
 AWS_SECRET_ACCESS_KEY
 AWS_ACCESS_KEY_ID

 You can do this by using the export command.  e.g.
 `export EDX_GPG_PASSPHRASE=abcdefg`

### Sample session:

```
mkdir s3_data
cd s3_data
edx_ls_course_data davidson
edx_download_latest tabular
edx_download_latest tracking
edx_process <the_data_file> <master_data_dir>
edx_process <the_data_file> <master_data_dir>
```

