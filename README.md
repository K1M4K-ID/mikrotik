# mikrotik cli
ip address add address=ip shared (bedakan akhir ip.100) interface=ether1

ip route add gateway=(gw ip shared)

ip dns set servers=ip gw,8.8.8.8 allow-remote-request=yes

ip firewall nat add chain=srcnat action=masquerade out-interface=ether1

# block url

^.+(youtube.com).*$
