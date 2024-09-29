# cloudflare-warp

(https://pkg.cloudflareclient.com/)

# Add cloudflare gpg key
curl -fsSL https://pkg.cloudflareclient.com/pubkey.gpg | sudo gpg --yes --dearmor --output /usr/share/keyrings/cloudflare-warp-archive-keyring.gpg


# Add this repo to your apt repositories
echo "deb [signed-by=/usr/share/keyrings/cloudflare-warp-archive-keyring.gpg] https://pkg.cloudflareclient.com/ $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/cloudflare-client.list

# edit
cd etc/apt/sources.list.d
sudo nano cloudflare-client.list
deb [signed-by=/usr/share/keyrings/cloudflare-warp-archive-keyring.gpg] https://pkg.cloudflareclient.com/ (lory main) --> change to jammy main

# Install
sudo apt-get update && sudo apt-get install cloudflare-warp


(https://developers.cloudflare.com/warp-client/get-started/linux/)


    Register the client (warp-cli registration new)
    Connect (warp-cli connect)

    Run (curl https://www.cloudflare.com/cdn-cgi/trace/) and verify that (warp=on). (optional)
