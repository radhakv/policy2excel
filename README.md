# policy2excel
NetBackup Policy to Excel tool

--Convert the Json policy out file to Excel
--Works for NetBackup 7.7.x and above


# Collecting the NetBackup policy output

Run bppllist command to collect the output
1. bppllist -allpolicies -compact_json > policy_out.json

# Setup Docker image

1. Download the docker file from the repo
2. 
