# NOT DONE YET SO PLEASE WAIT

# DISCLAIMER!!!
<sub>Unfortunately, since this could actually get me into legal trouble, I have to include this at the top :/<sub>
  
Everything here in this repository is for ***educational purposes only***, with the usage of such tools ***only*** intended for **testing** software or of the like *inside virtual machines*. I do **NOT** enourage people to pirate windows, or **any** of Microsoft's software. As a matter of fact, **NEVER** use this as a way to activate windows on a real computer, or a way to illegally obtain free software. **Buy the key!**

# Story time :)
Ok now that is out of the way, let me tell you a story. Naive me a couple years ago bought Microsoft Office 2016 standalone for 60 USD from a retailer named "BongoRolls" on Amazon. 

![](../main/ReadMe-Reference-Images/Wasted-60-dollars.PNG)

I was emailed the virtual disk image and the activation key. After installing office, I just let it sit there for a while, since I hadn't had a use for it during said 2 weeks. When I finally needed to use Excel and Powerpoint, I put the key in and guess what?
No work 😔. SOOOO I did what any reasonable person would do, and messaged the seller... waited for another week... and no reply. 

Okay, time to leave a review on the product to warn other users... the product was taken down 🙄. Fine! I'll review the seller then! Oop, apparently "I had not ordered anything from said seller"(product was taken down) 👺. I messaged them again, and in stronger words this time, but to this day, I still have not recieved any form of reply. I decided to get a refund, but after clicking on that button, apparently I had waited too long, and that my order was not eligible for one. What a joke! 

So therefore, I went on the internet and searched for a solution, and found the autoKMS method, which worked perfectly. I have subsequently experimented with the activation methods for most Microsoft software, and found ways to activate them.

Also yes, at that time, I thought about but didn't bother contacting Microsoft, and now, I doubt Microsoft would have done anything. Today, the order is still on the way. Just a wee bit too late though, as you can obviously see...

![](../main/ReadMe-Reference-Images/'Still-running-just-a-bit-late'.PNG)

# Overview...
In the repository, you can find tools to activate the following software ***for testing in virtual machines***, of course, which are, but **may be not limited to**:
  1) Windows 95 OSR 2 x86
  2) Windows 98 SE x86
  3) Windows XP SP3 Professional Corporate x64 and Professional x86
  4) Windows Vista Home Premium SP2 x86 and x64
  5) Windows 7 Ultimate x64
  6) Windows 8/8.1 Professional x64
  7) Windows 10 Professional x64
  8) Microsoft Office 2016
  9) Microsoft Office 2019
  10) Windows Server 2016(Datacenter, Essentials, Standard)
  11) Windows Server 2019(Datacenter, Essentials, Standard)

*Why the "may be not limited to"?* Well that's because these versions are either what I have installed in virtual machines and thus can confirm they work, or have seen them work when used by other people. However, since these tools are intended for a wide array of software versions, they will most likely work on other versions of said software as well.
  
# What about the virtual disk image files or media creation tools to install these?
Unfortunately, I do not have a collection of all of them, and as a result, the repository collection of these will be incomplete. One would need to surf the internet or ask a forum like reddit for such files that are missing from here.

# In-depth explanation for each of the tools included...
  1) autoKMS:
  
KMS, or Key Management Service is something developed my Microsoft themselves, aimed towards large organizations/companies, such that they can have an easier time managing all their computers OSes, especially since there can be a huge number of them. Said company hosts a local KMS server that will host all licenses the organization has purchased inside their own network, compared to each computer reaching Microsoft's servers to maintain their status of validity, over the internet. However, each computer has to contact the KMS server every 6 months to remain activated.

What the autoKMSes(**a big thanks to *msguides.com* for hosting the servers**) included here do is that they convert your retail/trial license into a volume license by changing the retail key into a generic volume license key. Then, it changes the default KMS server to contact into msguides's servers(i.e. kms***X***.MSGuides.com where X is a number) by default to activate the product and recontacts the server every 6 months to remain activated. Problems arise if the server is ever taken down, either by the developers of the server themselves, or by Microsoft if it decides to crack down on such unconvential activation methods. If the server is down by some means, your product would not be able to contact said server(every 6 months though, so if you still have like 3 months left before it needs to recontact the KMS server, per say, your product will remain activated for that 3 months) to remain activated and deactivate itself. 

However, note that these batch scripts are recently now detected by Windows Defender, Malwarebytes, Trend Micro, and most likely other antivirus software as something similar to "HackTool:Win32/AutoKMS", so please disable antivirus when running said script, and place it in a safe spot where your antivirus can't touch it.

Speaking of which, here's a guide on how to host/make your own KMS server(if link is down use archive.org or something):
https://docs.microsoft.com/en-us/deployoffice/vlactivation/configure-a-kms-host-computer-for-office

  2) Windows Loader
  
Alright, here is where it gets a bit hardcore. Your antivirus will definetely flag this as a "CRCK_KEYGEN" or "Hacktool:Win32/Keygen" or something similar, so make sure to turn it off when running, and keep the loader in a safe place. Secondly, if KB971033 windows update is installed, delete that update. It will make Windows Loader not work. Alright, not that is out of the way, let me explain this.

Microsoft has 3 different distribution channels for their products, namely retail, OEM, and volume license. AutoKMSes use the volume license to activate the product, but Windows Vista, and Windows 7 Home Premium/Ultimate only had retail and OEM licenses availible. This means that any autoKMS will not be able to use a volume license to connect to a KMS server to activate the product, because there isn't volume license to begin with. 

This is where Windows Loader by Daz comes in. 
