# Day 3 - [day 3 - 10-06-2026]

Today I learned basic networking commands on Linux. These are essential for reconnaissance and identifying network interfaces in penetration testing.

## Commands I practiced:

- `ifconfig` - Display and configure network interfaces (IP address, MAC, etc.)
- `iwconfig` - Configure wireless network interfaces (Wi-Fi specific)
- `dhclient` - Obtain an IP address from a DHCP server (dynamic IP)
- `dig` - DNS lookup utility; query domain name servers

## Examples I ran:


# Show all network interfaces
ifconfig

# Show only wireless interfaces
iwconfig

# Release and renew IP via DHCP
sudo dhclient -v eth0

# Query DNS records for a domain
dig google.com
dig -x 8.8.8.8   # reverse lookup

Notes:

· ifconfig is being replaced by ip command on newer Linux distros, but still widely used.
· iwconfig is crucial for Wi-Fi pentesting (monitor mode, channel hopping).
· dig gives more detailed info than nslookup; useful for finding mail servers, name servers.
· dhclient is useful when your interface doesn't get an IP automatically.
