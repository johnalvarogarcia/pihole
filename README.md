<h1>Implementing Pi-hole on a Synology NAS</h1>


<h2>Description</h2>
Pi-hole is a DNS sinkhole used for blocking ad traffic. We'll use Pi-hole, via Docker on our Synology NAS, as our DNS server and then setup blocklists to known ad serer lists to significantly reduce the amount of advertisements we see around the web.

First, we'll setup a Mac VLAN interface and a network bridge interface by connecting to our nas via SSH.

Then we'll download, configure, and initialize our Pi-hole container. We'll create environment variables including our admin account and it's password, along with pointing our container to our network bridge interface.

We can now start the container and access the Pi-hole GUI by navigating to our macvlan's IP and add several blocklists to Pi-hole to tune our web experience.

For this project we:
<ul>
  <li>Connect to our Synology NAS via SSh.</li>
  <li>Create a macvlan and network bridge interface.</li>
  <li>Create a resolve.conf file to add our nameservers.</li>
  <li>Download the Pi-hole container Using Docker/Container Manager.</li>
  <li>Initialize Pi-hole using our created bridge network.</li>
  <li>Configure Pi-hole admin account and directories.</li>
  <li>Add blocklists to Pi-hole to block advertisements.</li>
</ul>
<br />


<h2>Platforms and Technologies Used</h2>

- <b>Synology NAS</b> 
- <b>SSH</b>
- <b>Pi-Hole</b>
- <b>Terminal</b>


<h2>SSH into Synology</h2>

<p align="center">
<img src="https://i.imgur.com/kopEyNp.jpeg" height="80%" width="80%"/>
<br />
  <h2>Creating macvlan interface:</h2>

<p align="center">
  <img src="https://i.imgur.com/c2YuI4R.jpeg" height="80%" width="80%"/>
<br />  
<h2>Creating a network bridge interface:</h2>

<p align="center">
  <img src="https://i.imgur.com/dnegpTp.jpeg" height="80%" width="80%"/>
<br />
<h2>Pi-hole running and blocking ads:</h2>

<p align="center">
  <img src="https://i.imgur.com/HgWHA4U.jpeg" height="80%" width="80%"/>
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
