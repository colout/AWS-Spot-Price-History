# AWS-Spot-Price-History
Simple module to give historical pricing for spot EC2 instances.

Requires AWS CLI to be installed and usable from your machine's command line.  Also requires key/secret key to be setup through AWS configure.

Class takes to inputs: EC2 machine type (e.g. m1.xlarge) and number of months prior you wish to see spot prices for (e.g. 3).

AMI type and other information (e.g. region) can be changed by editing the os.system command passed to the AWS CLI on line 31 (function "describeSpotPrice()")

## Example usage: 

  	#Declare object:
  
  	#Input of AMI type and number of previous months to review.

	listPriceObject = comparePrice("t3.2xlarge", 3)
	

	#Calculate two different dates.

	listPriceObject.monthDelta()        
	

	#Submit AWS CLI shell command for describing spot instances prices.
	
	listPriceObject.describeSpotPrice()
