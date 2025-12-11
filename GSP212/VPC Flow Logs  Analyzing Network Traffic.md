<h1 align="center">
🚀  VPC Flow Logs - Analyzing Network Traffic
 || GSP212       🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml

curl -LO raw.githubusercontent.com/prateekrajput08/Arcade-Google-Cloud-Labs/refs/heads/main/VPC%20Flow%20Logs%20-%20Analyzing%20Network%20Traffic/TechCode.sh
sudo chmod +x TechCode.sh
./TechCode.sh

```

### Task 1 : vpc-flows

```lookml

export ZONE=$(gcloud compute instances list --filter="name=centos-clean" --format="value(zone)")
gcloud compute ssh centos-clean --zone=$ZONE --quiet

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
