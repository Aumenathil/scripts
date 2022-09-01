# scripts
# for ubuntu linux scripting
# Saved Scripts for Myself and Others

# This is useful to fetch info on an IP address. 
curl -s http://ipinfo.io/104.223.95.86


curl -s http://ipinfo.io/104.223.95.86 | grep country | sed 's/\"//g' | sed 's/\,//g' | awk -F" " '{print $2}' > IP_lookup.sh
nano IP_lookup.sh


# Inside here you want to place your curl code with the argument like this:
curl -s http://ipinfo.io/$1 | grep country | sed 's/\"//g' | sed 's/\,//g' | awk -F" " '{print $2}'
# save and exit
chmod +x IP_lookup.sh
./IP_lookup.sh

