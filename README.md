<h3>DNS Tunneling Using Sub-Domains</h3>

<p>
DNS is required for the Internet to work properly and as a result is ubiquitous. One way people have been seen exfiltrating data out of a network is with DNS. There are several ways to do this; you can stuff data into any DNS record, you could tunnel through the actual protocol UDP/53, and in this case we are just using subdomains.
</p>
<p>
In this case, using sub-domains, the adversary can encode the data, chop it into chunks, configure those chunks as sub-domains, then resolve those sub-domains from within the compromised environment, and wait for the requests to come to them and stitch them all together. 
</p>
<p>
The data in this example is dns_data.txt, a blueberry muffin recipe which is base64 encoded. The encoded data has been chopped up into consumable bites and prepended to a domain. Collection of each of these name resolutions on the other side would enable the adversary to put them back together and decode the data.
</p>
<p>
The actual command & control system to put the data back together is not provided as part of this POC.
</p>
<p>
You may have Set-Execution policy in Windows for this powershell script to run.
</p>
