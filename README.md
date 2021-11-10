# GCP-Storage-Explorer

The script iterates through all the available projects in your GCP account and extracts which compute engine instances can view which storage (e.g. can use the command gsutil ls on a storage).

The script enumerates which compute engine instance configured with at least one of the following permission:
('https://www.googleapis.com/auth/devstorage.read_only', 
'https://www.googleapis.com/auth/devstorage.read_write', 
'https://www.googleapis.com/auth/devstorage.full_control', 
'https://www.googleapis.com/auth/cloud-platform')

Review the output to easily analyze the viewing permissions on each bucket in order to prevent attackers from exposing data in your GCP environment and stay safe!

# Disclaimer
This tool is for testing and educational purposes only. 

Any other usage for this code is not allowed. Use at your own risk.

The author bears NO responsibility for misuse of this tool.

By using this you accept the fact that any damage caused by the use of this tool is your responsibility.

# Dependencies
1. Install the gcloud sdk prior running the script.
You can get the installation instructions for your OS here:
https://cloud.google.com/sdk/docs/install

2. Sudo apt-get install jq

# TODO
Add iteration for organizations level

# Author
<a href="https://twitter.com/ellicho007">Liat Vaknin</a> is an offensive security researcher @ <a href="https://twitter.com/orcasec?s=11">Orca Security</a>.
