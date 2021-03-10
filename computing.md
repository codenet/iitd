# Computing

Resources for setting up webpage/email clients/other software/etc: https://csc.iitd.ac.in/

## Accessing IITD internal website from outside campus
You need to setup VPN for this
* [Instructions to setup VPN (slides in pdf)](assets/COL106VPN.pdf)
> Note: Faculty members can request and approve their own VPN requests from [ldap link](https://ldap1.iitd.ac.in/usermanage/services.php).

## Setting up proxy on computer 
(Copied from https://compiler.ai/dev/proxy.html)

### Accessing internet on server machine
* Server machines do not have direct internet connection and, like other department machines, you need to login into proxy server before you can access internet. The following steps show how to login into proxy server using the [iitd-login.py](https://compiler.ai/dev/iitd-login.py) script.
* As the server is shared by many users, we advise that you remain logged-in into proxy server only while you need internet connection and disconnect as soon as possible.

### HOWTO login into proxy server without GUI using iitd-login.py script
* Setup environment variables for your proxy server. For e.g., for PhD students `http_proxy` (and friends) need to be set to `http://proxy61.iitd.ac.in:3128`.
* The exhaustive list of variables is: `http_proxy`, `https_proxy`, `HTTP_PROXY`, `HTTPS_PROXY`.
* Download the [iitd-login.py](https://compiler.ai/dev/iitd-login.py) script and copy it to your home directory.
* In the script, change `PROXY_BASE_URL` to the URL for your proxy (for e.g., it is `proxy61.iitd.ac.in` for PhD students).
* Start a tmux session: tmux
* Launch the login script: `env -u http_proxy -u https_proxy -u HTTP_PROXY -u HTTPS_PROXY python3 iitd-login.py -d`
* Provide credentials
* On success, the message "Logged in." will be printed (along with other messages).
* Detach from the tmux session using `C-b d (Ctrl+B followed by d)`
* Do your git pull etc.
* Attach to tmux session with tmux a
* Hit `C-c` to logout from proxy server.
* Exit from shell to close tmux session.

## Mailing lists
Faculty forum https://lists.iitd.ac.in/cgi-bin/mailman/listinfo/faculty_forum
* Informal chat among faculty members

