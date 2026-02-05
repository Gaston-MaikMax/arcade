<h1 align="center">
🚀  Assign External IP to VM Instance using gcloud
 ||        🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml

export VM_NAME=$(gcloud compute instances list --format='value(name)' --limit=1) && export ZONE=$(gcloud compute instances list --format='value(zone)' --limit=1) && export REGION=${ZONE%-*}
gcloud compute addresses create lab-static-ip --region=$REGION
export IP_ADDRESS=$(gcloud compute addresses describe lab-static-ip --region=$REGION --format='get(address)') && gcloud compute instances add-access-config $VM_NAME --zone=$ZONE --address=$IP_ADDRESS
## Iska bhi Credit chahiye kya?😂

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
