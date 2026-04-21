#Steps to implement 
1. Create an EC2 instance. ( default EBS is assigned to the instance)
2. Create snapshots in EC2 for this volume. (This can be an ideal scenario where an organization might be storing the data )
3. Now create a lambda function to check EC2 instances and volumes.
4. Once created, try DEPLOY & TEST. If it fails for permissions, go to the 'permissions' tab and then to 'role'. Create a new policy or search and attach some policies from the policies tab.
5. Once attached, try 'test' again.
6. If the tests are fine, now delete the EC2 instance created. This would delete the default volume.(snapshot is still there)
7. Now run the lambda function, and it should automatically delete the snapshot of the volume that is non-existent.
