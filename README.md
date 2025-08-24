curl -fsSL https://amrography.github.io/debian-mirror/myrepo.gpg | sudo gpg --dearmor -o /usr/share/keyrings/myrepo.gpg
echo "deb [signed-by=/usr/share/keyrings/myrepo.gpg] https://<username>.github.io/<repo> stable main" | sudo tee /etc/apt/sources.list.d/myrepo.list
sudo apt update
