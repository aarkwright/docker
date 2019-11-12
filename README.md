# One-liner
```bash
docker run -d --name nessus --restart unless-stopped -e VERSION=8.8.0 -v nessus_data:/opt/nessus -p 8834:8834 aarkwright/nessus
```

# Details
```bash
docker run -d \               # Run detached;
--name nessus \               # Give it a nice name;
--restart unless-stopped \    # [optional] Have it automatically restart, unless you manually stop it;
-e VERSION=8.8.0 \            # [optional] Specify the version string (default: 8.8.0)
-v nessus_data:/opt/nessus \  # [recommended] Store the Nessus data in a local volume; you can also specify a local filesystem path
-p 8834:8834 \                # [optional] Expose the webapp port
aarkwright/nessus 
```
