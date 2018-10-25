SOLUTION:

This is a Tor exit relay, so the best I am able to do on my end is prevent traffic from going to the specified target IPs. However, this is not recommended as it will prevent legitimate Tor users (possibly in oppressed countries, as is my goal with being an operator - reducing digital censorship) from accessing services running on those IPs. I can also suggest that the server operator temporarily block the Tor network or my specific relay, though for the 2nd solution, the attacker will just reroute to a different exit relay and the process would repeat. There are guides on how to block Tor, and I have provided them in the abuse email. I have also provided resources to assist in reducing the frequency of SSH attacks in general, not just from Tor.

RESPONSE:

Hi,

I'm sorry for the trouble. The IP you quote hosts a Tor exit node (open relay).

You can block our IP address, but the abuser doesn't use our relays specifically; he/she will just be routed through a different exit node outside of our control instead.

You could block Tor temporarily from your side. Please only issue a temporary block to not affect other, legitimate users of Tor.

Tor is a research project, funded by the National Science Foundation and previously DARPA (among others). Its primary goal is to provide people from hostile environments with encrypted and uncensored access to the Internet. For more than a third of the world's population, the Internet is being either filtered or monitored. Every day, activists and bloggers are imprisoned or threatened for what we in other countries see as basic human rights.

There are usage stats on the www.torproject.org website that show that more than 500,000 users from China, Iran and similar regimes (have to) use Tor to access the Internet every day.

I hope that you understand the importance of Tor, and don't block the whole Tor network because of a single attack/misuse.

I can also offer the following suggestions:

Many worms, scanners, and botnets scan the entire Internet looking for SSH logins (especially on port 22). The fact that a few logins happened to come from Tor is likely a small blip on your overall login attempt rate. You might also consider a rate limiting
solution: https://kvz.io/blog/2007/07/28/block-brute-force-attacks-with-iptables/

If it is in fact a serious problem specific to Tor, the Tor project provides an automated DNSRBL for you to query to block login attempts coming from Tor nodes: https://www.torproject.org/projects/tordnsel.html.en

It is also possible to download a list of all Tor exit IPs that will connect to your SSH port: https://check.torproject.org/cgi-bin/TorBulkExitList.py?ip=YOUR_IP&port=22

You can use this list to create iptables rules to block the network. However, we still recommend using the general approach, as the attack will likely simply reappear from an open proxy or other IP once Tor 
is blocked.

Thank you for your understanding. If you have further questions, feel free to contact us again.
