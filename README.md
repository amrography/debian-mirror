
```sh
curl -fsSL https://amrography.github.io/debian-mirror/myrepo.gpg | sudo gpg --dearmor -o /usr/share/keyrings/amrography-debian.gpg
echo "deb [signed-by=/usr/share/keyrings/amrography-debian.gpg] https://amrography.github.io/debian-mirror stable main" | sudo tee /etc/apt/sources.list.d/amrography-debian.list
sudo apt update
```
