To start Lampp automatically on startup, you can create a systemd service. Here's how you can do it:

1. Create a new service unit file for Lampp:
```
sudo nano /etc/systemd/system/lampp.service
```

2. Add the following lines to the file:
```
[Unit]
Description=XAMPP

[Service]
ExecStart=/opt/lampp/lampp start
ExecStop=/opt/lampp/lampp stop
Type=oneshot
RemainAfterExit=true

[Install]
WantedBy=multi-user.target
```

3. Save and close the file.

4. Reload systemd to pick up the changes:
```
sudo systemctl daemon-reload
```

5. Enable the service to start automatically on boot:
```
sudo systemctl enable lampp.service
```

Now, Lampp should start automatically on system startup. You can manually start and stop it using `sudo systemctl start lampp` and `sudo systemctl stop lampp`, respectively.
