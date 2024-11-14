# Mitigate Threats and Vulnerabilities with Security Command Center: Challenge Lab || [GSP382]() ||

### **Solution Video:** [Watch Here]()

### Step 1 .

```
gcloud scc muteconfigs create muting-flow-log-findings --project=$DEVSHELL_PROJECT_ID --location=global --description="Rule for muting VPC Flow Logs" --filter="category=\"FLOW_LOGS_DISABLED\"" --type=STATIC && gcloud scc muteconfigs create muting-audit-logging-findings --project=$DEVSHELL_PROJECT_ID --location=global --description="Rule for muting audit logs" --filter="category=\"AUDIT_LOGGING_DISABLED\"" --type=STATIC && gcloud scc muteconfigs create muting-admin-sa-findings --project=$DEVSHELL_PROJECT_ID --location=global --description="Rule for muting admin service account findings" --filter="category=\"ADMIN_SERVICE_ACCOUNT\"" --type=STATIC

```

### Step 2 .

```
curl -LO raw.githubusercontent.com/Techcps/GSP-Short-Trick/master/Mitigate%20Threats%20and%20Vulnerabilities%20with%20Security%20Command%20Center%3A%20Challenge%20Lab/techcps1.sh
sudo chmod +x techcps1.sh
./techcps1.sh

```

#### static-ip

### Step 3 .

```
curl -LO raw.githubusercontent.com/Techcps/GSP-Short-Trick/master/Mitigate%20Threats%20and%20Vulnerabilities%20with%20Security%20Command%20Center%3A%20Challenge%20Lab/techcps2.sh
sudo chmod +x techcps2.sh
./techcps2.sh

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
