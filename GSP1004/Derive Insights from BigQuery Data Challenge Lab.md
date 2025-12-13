<h1 align="center">
🚀  Interacting with Vault Policies
 || GSP1004        🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml


curl -LO raw.githubusercontent.com/prateekrajput08/Arcade-Google-Cloud-Labs/refs/heads/main/Interacting%20with%20Vault%20Policies/TechCode1.sh
sudo chmod +x TechCode1.sh
./TechCode1.sh

```

### Task 2

```lookml


run() {
  echo -e "\n\033[1;36m▶ $*\033[0m"
  "$@"
  echo -e "\n\033[1;33mPress ENTER to continue...\033[0m"
  read
}

export VAULT_ADDR='http://127.0.0.1:8200'
run vault status
printf "\033[1;32mEnter Vault Token: \033[0m"
read -s ROOT_TOKEN
echo
run vault login token="$ROOT_TOKEN"
run vault secrets list
run vault auth enable userpass
run vault write auth/userpass/users/example-user password='password!'
run vault login -method=userpass username=example-user password='password!'
run vault secrets list
echo -e "\n\033[1;32mAll commands completed. Shell will stay open.\033[0m"
exec bash


```

### Task 3

## ⚓Create Policy demo-policy

```lookml


path "sys/mounts" {
    capabilities = ["read"]
}

```

### Task 4

## ⚓Generated Token's Policies demo-policy

```lookml


run() {
  echo -e "\n\033[1;36m▶ $*\033[0m"
  "$@"
  echo -e "\n\033[1;33mPress ENTER to continue...\033[0m"
  read
}

run vault secrets list
run vault login -method=userpass username=example-user password='password!'
run vault secrets list
printf "\033[1;32mEnter Vault Token: \033[0m"
read -s YOUR_TOKEN
echo
run vault token capabilities "$YOUR_TOKEN" sys/mounts
run vault token capabilities "$YOUR_TOKEN" sys/policies/acl
run vault policy list


```

### Task 5

## ⚓Edit Policy demo-policy

```lookml


path "sys/policies/acl" {
    capabilities = ["read", "list"]
}

```

### Task 6

```lookml


run() {
  echo -e "\n\033[1;36m▶ $*\033[0m"
  "$@"
  echo -e "\n\033[1;33mPress ENTER to continue...\033[0m"
  read
}

run vault policy list
vault policy list > policies.txt
echo "policies.txt created"
run vault token capabilities "$YOUR_TOKEN" sys/policies/acl
vault token capabilities "$YOUR_TOKEN" sys/policies/acl > token_capabilities.txt
echo "token_capabilities.txt created"
export PROJECT_ID=$(gcloud config get-value project)
run gsutil cp policies.txt token_capabilities.txt "gs://$PROJECT_ID"
```

### Task 7

```lookml

curl -LO raw.githubusercontent.com/prateekrajput08/Arcade-Google-Cloud-Labs/refs/heads/main/Interacting%20with%20Vault%20Policies/TechCode2.sh
sudo chmod +x TechCode2.sh
./TechCode2.sh

```

### Task 8

```lookml


curl -LO raw.githubusercontent.com/prateekrajput08/Arcade-Google-Cloud-Labs/refs/heads/main/Interacting%20with%20Vault%20Policies/TechCode3.sh
sudo chmod +x TechCode3.sh
./TechCode3.sh

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
