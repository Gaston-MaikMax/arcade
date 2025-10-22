<h1 align="center">
🚀  Configuring IAM Permissions with gcloud
 || GSP647        🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1.

```lookml

export ZONE=$(gcloud compute project-info describe \
--format="value(commonInstanceMetadata.items[google-compute-default-zone])")
gcloud compute ssh centos-clean --zone=$ZONE --quiet

```

### Task 2.**``**

```lookml

curl -LO raw.githubusercontent.com/prateekrajput08/Arcade-Google-Cloud-Labs/refs/heads/main/Configuring%20IAM%20Permissions%20with%20gcloud/TechCode.sh
sudo chmod +x TechCode.sh
./TechCode.sh

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
