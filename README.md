Credits to [https://gist.github.com/jwalanta/53f55d03fcf5265938b64ffd361502d5](https://forum.openwrt.org/t/openwrt-detect-new-device-and-send-text-message-mail/147555/12) i just edit it to my needs

# Create Telegram Bot
[https://core.telegram.org/bots/tutorial](https://core.telegram.org/bots/tutorial)

# The script
Save the **90-newdev** file at **/etc/hotplug.d/dhcp** and give execute permisiion

# Dump the current known devices to /etc/known_macs
cat /tmp/dhcp.leases | awk '{ print $2" "$3" "$4 }' >/etc/known_macs
