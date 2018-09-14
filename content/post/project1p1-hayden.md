---
title: "Project 1 - Post 1: Hayden"
author: "Hayden Wilcoz"
cover: "/img/cover.jpg"
tags: ["tagA", "tagB"]
date: 2018-09-13T11:05:21-07:00
draft: false
---
<body>
<h3>Hayden Wilcox:</h3><br>
Assigned Task: Research Ansible and Practice various components and concepts:<br>
	<p style="margin-left:4em> ·  Issues arose when attempting to update Oracle Virtual Box, had to delete previous Ubuntu virtual machine and reinstall.<br>
							   ·  Reinstalled git related commands and re-accessed GitHub to download branches<br></p>
<small> o &emsp; Due to adding two-factor authentification onto GitHub, I had to learn how to generate a Personal Access Token to allow myself access onto the site via ssh: </small><br>
	<small>&emsp; &emsp; &emsp; &emsp;·   Cloned branch to be used with Ansible </small><br>
	<small>&emsp; &emsp; &emsp; &emsp;·   Setup a personal AWS ubuntu server, using default settings. </small><br>
	<small>&emsp; &emsp; &emsp; &emsp;·   Added the ability for it to be connected via http/s and port :1313 similar to project 1, just in case.</small><br>
	<small>&emsp; &emsp; &emsp; &emsp;·   Had difficulties ssh-ing into the instance, attempted to convert .pem file to .ppk as I did in the prior project, but had no success. <br> 
	   &emsp;&emsp; &emsp; &emsp;&emsp;&emsp; &emsp;&emsp; - .pem file had to be put onto the VM via usb stick, and had to be included in every ssh command.</small><br>
<small>o &emsp; ssh process was simplified by creating a simple script “ubussh” which contains the line “ssh -i /home/hayden/hayden-test-keys.pem ubuntu@13.58.31.238”<br>
	o &emsp; Gave the file execution permission with chmod +x<br>
	o &emsp; Doing this made the ssh process easier, as I no longer had to recall the IP or type out the lengthy command, simply ./ubussh<br> 
<div style="margin-left:4em">·   Began following a guide in order to practice using Ansible and use it to setup Nginx. This caused some issues. </div>
			<div style="margin-left:9em">	- It recommended creating a new user to use when performing commands. This proved unnecessary, and also caused a security flag on the .pem file as there was now another user without necessary permissions able to access it. This was solved with chmod +600. </div>
<div style="margin-left:4em">·   I used ssh-keygen and added the key to authorized_keys file on the instance, but this proved unnecessary as I did not use the extra user. <br>
	·   Attempted to ping AWS instance, had numerous difficulties. Used the hosts file as my inventory file, but was advised to set up a dynamic inventory file for this purpose later. Research needed. <br>
	·   In order to ping AWS instance, I needed to install Ansible and Python onto the instance itself. <br>
			&emsp;&emsp; &emsp;&emsp; - Initially misunderstood the directions and installed Python onto client VM. <br>
	·   Python3 was installed on the AWS instance, but the ansible interpreter did not point to it. <br>
		&emsp;&emsp; &emsp;&emsp; - Needed to use the command ansible_interpreter_path=/usr/bin/python3 <br>
	·   Was finally able to ping the instance then moved on to attempting to use a playbook to set up nginx. <br>
	·   Had a few issues with formatting, but these were fixed with a web based formatting software<small> <br> </div> </small>
Made some slight edits to the playbook to fix a connection issue, adding ports etc. but ultimately was unable to get the playbook to work. The screenshot provided is the current error being displayed at the time of writing:<br>
	![Screenshot](/img/sh-hayden.png) <br>
Side note: learned a few shortcuts when using vim to make editing files easier and quicker, such as “dG” to clear the entire file, and “u” to undo actions.
</body>
