<h1 align="center">
🚀  Enhance Scalability Using Managed Instance Groups
 ||        🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml


gcloud compute instance-groups managed create dev-instance-group --template=dev-instance-template --size=1 --region=[enter region] && gcloud compute instance-groups managed set-autoscaling dev-instance-group --region=[enter region] --min-num-replicas=1 --max-num-replicas=3 --target-cpu-utilization=0.6 --mode=on


```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
