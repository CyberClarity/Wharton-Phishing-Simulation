# Ngrok Setup Notes

## 🎯 Purpose
Ngrok was used to tunnel the local Gophish phishing server, making it accessible to the target over the public internet.

---

## 🚀 Steps to Set Up Ngrok with Gophish

1️⃣ **Download & Install Ngrok**
- Go to [ngrok.com/download](https://ngrok.com/download) and download the binary for your OS.
- Unzip and place it in a directory in your PATH.
- (Optional) Add your authtoken:
```bash
ngrok config add-authtoken <your-ngrok-authtoken>
```

Start Gophish
Launch your Gophish server locally (default: http://127.0.0.1:80 or another port you configured).
```bash
./gophish
```
Expose Gophish with Ngrok
Open a new terminal window.
Run ngrok to tunnel your Gophish server port. For example, if Gophish is running on port 80:
```bash
ngrok http 80
```

Ngrok will generate a public URL like:
```bash
Forwarding                    https://abc12345.ngrok.io -> http://localhost:80
```

Use the Ngrok URL:
```bash
Insert this Ngrok URL into your phishing emails’ links, so the victim can access your phishing landing page outside your network.
```

# Example Command Recap

# Start Gophish:
```bash
./gophish
```
# In another terminal, tunnel port 80 with ngrok"
```bash
ngrok http 80
```

Notes & Security:
```bash
-Keep the ngrok tunnel active while the phishing campaign runs, or the link will break.
-Remember ngrok tunnels change each time you restart ngrok, unless you use a reserved domain (paid ngrok plan).
-Never use phishing skills maliciously — always test ethically with permission.
```

