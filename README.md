# ServerSetup
My orcale server setup script!

## To use a webhook:

> Must have a domain in cloudflare; take from freemnom then transfer it to there.
> After that go to tunnels & make a tunnel for free and setup it in the server ( follow the on screen steps.).
> Take the url use paste it in url of webhook of bot.
> Now do screen then set port for ex. 443 which has been provided in the local host url of cloudflare tunnel; then ```sudo su``` then activate virtual env then cd and run it.
> Must do ```git config --global --add safe.directory /home/ubuntu/folder``` for git pull support and ```sudo chown -R ubuntu /home/ubuntu/venv/``` for pip3.

## Open port in orcale:
```
sudo apt install firewalld
```
```
sudo firewall-cmd --zone=public --permanent --add-port=443/tcp
```
```
sudo firewall-cmd --reload
```
```
sudo iptables -I INPUT -m state --state NEW -p tcp --dport 443 -j ACCEPT
```
```
sudo netfilter-persistent save
```
> Then open in the protal!
