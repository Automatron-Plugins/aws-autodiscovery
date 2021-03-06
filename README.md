# AWS autodiscovery plugin for Automatron

This is a simple Autodiscovery plugin for Automatron that will discover EC2 instances


## Installation

Place `aws` directory into the Automatron `plugins/discovery/` directory.

```shell
$ cp -r aws plugins/discovery/
```

Install Python dependencies with `pip`.

```shell
$ pip install -r requirements.txt
```

## Configuration

This plugin does require some configuration in Automatron's master configuration file `config.yml`.

```yaml
discovery:
  plugins:
    aws:
      aws_access_key_id: example
      aws_secret_access_key: example
      interval: 60
      filter:
        - PublicIpAddress
        - PrivateIpAddress
```

The `aws` plugin requires four configuration items.

* `aws_access_key_id` - This an Key ID for AWS
* `aws_secret_access_key` - This is the secret key used to authenticate with AWS
* `interval` - This is the frequency to query Digital Ocean's API
* `filter` - This is used to define whether Public or Private IP addresses are used for target identification 

