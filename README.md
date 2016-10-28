# AMIEraser

This is yet another tool you can use to delete Amazon Machine Images (AMIs)
from your AWS account. It will deregister the image and also delete
the snapshots associated with that image so they aren't "orphaned" after
the AMI is gone.

## Requirements

* boto3
* AWS credentials in the [saved credential file](http://boto3.readthedocs.io/en/latest/guide/configuration.html#interactive-configuration)

## Running the tool

You should be able to just run the amieraser.py script.

Options:

    Usage: amieraser.py [options]

    Options:
      -h, --help         show this help message and exit
      --id=ID            One or more AMI Ids in a comma-seperated list. IDs take
                         the form 'ami-xxxxxxxx'
      --region=REGION    The Amazon region the AMIs are located in. us-east-1 is
                         used by default
      --profile=PROFILE  The name of the profile in your AWS credentials file. If
                         not specified, the default profile is used

## Future Enhancements

* Packaging as a more proper Python module/program, not just a random script
* Search by AMI name?
