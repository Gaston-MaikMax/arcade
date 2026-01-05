<h1 align="center">
🚀  GKE Autopilot: Qwik Start
 || GSP957        🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml


 https://github.com/subfuzion/voting-demo.git


```

### Task 2

```lookml


#!/bin/bash

# Bright Foreground Colors
BLACK_TEXT=$'\033[0;90m'
RED_TEXT=$'\033[0;91m'
GREEN_TEXT=$'\033[0;92m'
YELLOW_TEXT=$'\033[0;93m'
BLUE_TEXT=$'\033[0;94m'
MAGENTA_TEXT=$'\033[0;95m'
CYAN_TEXT=$'\033[0;96m'
WHITE_TEXT=$'\033[0;97m'

NO_COLOR=$'\033[0m'
RESET_FORMAT=$'\033[0m'
BOLD_TEXT=$'\033[1m'
UNDERLINE_TEXT=$'\033[4m'

# Displaying start message
echo
echo "${CYAN_TEXT}${BOLD_TEXT}╔════════════════════════════════════════════════════════╗${RESET_FORMAT}"
echo "${CYAN_TEXT}${BOLD_TEXT}|                      LearnWithAshish                   |${RESET_FORMAT}"
echo "${CYAN_TEXT}${BOLD_TEXT}╚════════════════════════════════════════════════════════╝${RESET_FORMAT}"
echo
gcloud auth list
export REGION=$(gcloud compute project-info describe --format="value(commonInstanceMetadata.items[google-compute-default-region])")
export PROJECT_ID=$(gcloud config get-value project)
gcloud config set compute/region "$REGION"
gcloud container clusters get-credentials dev-cluster --region $REGION
cd ~/voting-demo/v2

skaffold run --default-repo=gcr.io/$PROJECT_ID/voting-app --tail

kubectl get svc web-external --output=json | jq -r .status.loadBalancer.ingress[0].ip

web_external_ip=$(kubectl get svc web-external --output=json | jq -r .status.loadBalancer.ingress[0].ip)

echo
echo -e "\033[1;33mhttp://$web_external_ip\033[0m"
echo
echo -e "\033[1;33mhttp://$web_external_ip/results\033[0m"
echo

while true; do
    echo -ne "\e[1;93mDo you Want to proceed? (Y/n): \e[0m"
    read confirm
    case "$confirm" in
        [Yy])
            echo -e "\e[34mRunning the command...\e[0m"
            break
            ;;
        [Nn]|"")
            echo "Operation canceled."
            break
            ;;
        *)
            echo -e "\e[31mInvalid input. Please enter Y or N.\e[0m"
            ;;
    esac
done

skaffold delete

curl -ks https://`kubectl get svc frontend -o=jsonpath="{.status.loadBalancer.ingress[0].ip}"`/version
echo
echo -e "\e[41;97m🎉${WHITE}${BOLD} Congratulations for completing the Lab! 🎉 \e[0m"
echo
echo "📺 Subscribe to the channel: https://www.youtube.com/channel/UChSkWopRk1ErP2i0k4aa0KQ"
echo


```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
