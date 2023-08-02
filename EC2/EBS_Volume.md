# EBS_Volume
EBS (Elastic Block Store) Volume is a network drive, like a network USB
-  Can only be mounted to one instance at a time
-  Bound to a specific availability zone

# EBS Snapshot
- Make a backup of EBS at a point
- Archive (Cheaper storage)
- Recycle Bin (Recovery)
- Fast Snapshot Restore (FSR): expensive no latency full restore

# AMI
Amazon Machine Image
- Customized instance (software, configuration, OS...)
- For specific region
## AMI Process
1. Create a instance.  
2. Stop it and make a AMI.
3. Create a new instance with AMI.

