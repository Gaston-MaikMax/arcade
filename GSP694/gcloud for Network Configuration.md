<h1 align="center">
🚀  gcloud for Network Configuration
 || GSP694       🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml

gcloud compute firewall-rules create labnet-allow-internal --network=labnet --action=ALLOW --rules=icmp,tcp:22 --source-ranges=0.0.0.0/0

```

### Task 2

```lookml

gcloud compute firewall-rules create privatenet-deny --network=privatenet --action=DENY --rules=icmp,tcp:22 --source-ranges=0.0.0.0/0

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
