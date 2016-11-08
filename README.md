# policy2excel
NetBackup Policy to Excel tool

--Convert the Json policy out file to Excel
--Works for NetBackup 7.7.x and above


# Collecting the NetBackup policy output

Run bppllist command to collect the output
1. bppllist -allpolicies -compact_json > policy_out.json

# Setup Docker image

1. Download the docker file from the repo to policy2excel folder
2. run 'docker build  -t policy2excel policy2excel'

# Running the tool
1. Copy the file to a local directory eg: /var/tmp/data
2. docker run --rm -it --name policy2excel -v "/var/tmp/data":/root -w /root policy2excel:latest /usr/local/bin/policy2excel/policy2excel -i policy_out.json -o policy_out.xlsx --generate_excel

