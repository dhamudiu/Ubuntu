```
sudo /opt/lampp/lampp start
sudo /opt/lampp/lampp stop
sudo /opt/lampp/lampp restart
```

You can create short aliases for the above commands in your Ubuntu terminal. Open your terminal and follow these steps:

1. Open the `.bashrc` file in your home directory using a text editor like nano or vim:
```
nano ~/.bashrc
```

2. Scroll to the bottom of the file and add the following lines:
```
alias lamppstart='sudo /opt/lampp/lampp start'
alias lamppstop='sudo /opt/lampp/lampp stop'
alias lampprestart='sudo /opt/lampp/lampp restart'
```

3. Save and close the file.

4. To apply the changes, either restart your terminal or run:
```
source ~/.bashrc
```

Now you can use these shortened commands in your terminal:
```
lamppstart    # to start Lampp
lamppstop     # to stop Lampp
lampprestart  # to restart Lampp
```