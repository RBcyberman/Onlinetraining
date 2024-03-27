<h1>Threat Hunting Workshop: Hunting For Initial Access with Cyborg Security using Elastic KQL query </h1>

<h2>Description</h2>
Established in 2019 and headquartered in Florida, USA, Cyborg Security brings together a diverse group of threat hunters, threat intelligence analysts, and security researchers from across North America. Cyborg Security's mission is to equip organizations with the tools and knowledge necessary for preemptive defence against cyber threats, offering advanced threat-hunting services and expertise.
<br />
<br />
Cyborg Security launched an innovative, interactive threat-hunting workshop focused on the MITRE ATT&CK Tactic of INITIAL ACCESS. This immersive experience provides hands-on learning in a dynamic environment, led by expert threat hunters. Learners will explore the mechanics of impact and adversary tactics, using real-life data in a state-of-the-art hunting environment. Attendees gain free access to premium hunting tools, a community forum for networking, and upon completion, a Level I Threat Hunting certification and badge.
  
<br />


<h2>Tools or Utilities Used</h2>

- <b>Elastic Kibana SIEM</b>

<h2>Environments Used </h2>

- <b>Oracle VM Virtualbox</b> 
- <b>Open Virtualization Format Archive (.ova) file provided by Cyborg Security</b>

<h2>Configuration walk-through:</h2>

<p align="center">
First, I had to perform some configuration tasks, such as importing the OVA file, modifying the network settings of the type 2 hypervisor to bridge mode, identifying my IP address, and then downloading the lab log data before proceeding.<br/>
  
<img src="https://imgur.com/ChS3M2o.png" height="80%" width="80%" alt="onlinetraining"/>
<img src="https://imgur.com/V0wVU7V.png" height="80%" width="80%" alt="onlinetraining"/>
<br />
<br />
<br />
Then, guided by the host and the guideline document, I proceeded to conduct the threat hunt step by step. The document provided only keywords and directions rather than clear instructions, emphasizing the importance of self-guided discovery as a core aspect of the threat hunting process.<br/>
  
<img src="https://imgur.com/HTiSBei.png" height="80%" width="80%" alt="onlinetraining"/>
<img src="https://imgur.com/So3WPkk.png" height="80%" width="80%" alt="onlinetraining"/>
<br />
<br />
<br />
Now,  our task was to locate a malicious document within the log and then determine the timing of a potential unauthorized access event, including the process name, event PID, and any actions performed via the registry.

<img src="https://imgur.com/IUqiCBr.png" height="80%" width="80%" alt="onlinetraining"/>
<img src="https://imgur.com/gHLRW8e.png" height="80%" width="80%" alt="onlinetraining"/>
<br />
<br />
<br />
By paying close attention, I eventually identified a suspicious "svchost" process name linked to an unusual process.command.line value. Event codes 4688 and 4689 in the Active Directory log indicate process startup and termination, respectively. Additionally, by examining the process.parent.name and PID, we were able to piece together the entirety of the malicious process through the parent-child relationship.

<img src="https://imgur.com/LXzhSEA.png" height="80%" width="80%" alt="onlinetraining"/>
<img src="https://imgur.com/Bs8qfQk.png" height="80%" width="80%" alt="onlinetraining"/>
<br />
<br />
<br />
Finally, the Q&A session encouraged us to explore its free learning platform for additional hands-on exercises. Upon visiting, I found an array of resources for further learning and experimentation. To conclude, participants were presented with a challenge to earn a Credly badge by answering a question about the event code that verifies whether a scheduled task was created successfully or unsuccessfully. After my investigation, it turned out to be either event code 4698 or 4699.
<br />
<br />
Thus, I earned my badge, and overall, it was a comprehensive, rewarding, and enjoyable learning experience. I really appreciate the effort they put into making this available for free! Additionally, receiving an endorsement from the company on LinkedIn was a great opportunity to expand my professional network.

<img src="https://imgur.com/VAuLoKW.png" height="80%" width="80%" alt="onlinetraining"/>
<img src="https://imgur.com/7D3q07Y.png" height="80%" width="80%" alt="onlinetraining"/>
<img src="https://imgur.com/KjZo4L7.png" height="80%" width="80%" alt="onlinetraining"/>
<br />
<br />
</p>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
