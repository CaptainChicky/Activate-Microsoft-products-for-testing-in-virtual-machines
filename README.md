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
Unfortunately, literally 90% of them are greater than 2 GB, meaning I can't even put them in the "releases" section. This means that, unfortunately, I will not be able to supply them to you. I *can* provide some resources to get them though.

**Places to get virtual disk images, working and *safe* as of December 5th, 2020**:
  - https://tb.rg-adguard.net/public.php
  - https://winworldpc.com/library/operating-systems
  - https://www.heidoc.net/joomla/technology-science/microsoft/67-microsoft-windows-and-office-iso-download-tool (.exe file)
  - https://www.microsoft.com/en-us/software-download/windows8ISO
  - https://www.microsoft.com/en-US/Download/confirmation.aspx?id=7120 (will directly start downloading once clicked)
  - https://www.microsoft.com/en-us/Download/confirmation.aspx?id=18242 (will directly start downloading once clicked)
  - https://isoriver.com/
  - https://archive.org/details/operatingsystemcds
  - https://web.archive.org/web/20180704214535/http://mirror.corenoc.de/digitalrivercontent.net/

# In-depth explanation for each of the tools included...
  1) autoKMS
  
Please visit [msguides](https://msguides.com/) for the source. No registration needed.

KMS, or Key Management Service is something developed my Microsoft themselves, aimed towards large organizations/companies, such that they can have an easier time managing all their computers OSes, especially since there can be a huge number of them. Said company hosts a local KMS server that will host all licenses the organization has purchased inside their own network, compared to each computer reaching Microsoft's servers to maintain their status of validity, over the internet. However, each computer has to contact the KMS server every 6 months to remain activated.

What the autoKMSes(**a big thanks to *msguides.com* for hosting the servers**) included here do is that they convert your retail/trial license into a volume license by changing the retail key into a generic volume license key. Then, it changes the default KMS server to contact into msguides's servers(i.e. kms***X***.MSGuides.com where X is a number) by default to activate the product and recontacts the server every 6 months to remain activated. Problems arise if the server is ever taken down, either by the developers of the server themselves, or by Microsoft if it decides to crack down on such unconvential activation methods. If the server is down by some means, your product would not be able to contact said server(every 6 months though, so if you still have like 3 months left before it needs to recontact the KMS server, per say, your product will remain activated for that 3 months) to remain activated and deactivate itself. 

However, note that these batch scripts are recently now detected by Windows Defender, Malwarebytes, Trend Micro, and most likely other antivirus software as something similar to "HackTool:Win32/AutoKMS", so please disable antivirus when running said script, and place it in a safe spot where your antivirus can't touch it.

Speaking of which, [here's](https://docs.microsoft.com/en-us/deployoffice/vlactivation/configure-a-kms-host-computer-for-office) a guide on how to host/make your own KMS server(if link is down use archive.org or something).

![](../main/ReadMe-Reference-Images/autoKMS-preview.jpg)

  2) Windows Loader
  
Please visit [Daz's MyDigitalLife forum page](https://forums.mydigitallife.info/threads/58464-Windows-Loader-Download) for the source. Registration required. Here are also [two](https://forums.mydigitallife.net/threads/window-7-64-daz-loader-uefi-motherboard-disabling-uefi-will-work.34528/) further [links](https://forums.mydigitallife.net/threads/you-can-activate-win7-on-a-gpt-partition-with-daz-loader-without-converting-gpt-mbr.76768/) viewable without registration.
  
Alright, here is where it gets a bit hardcore. Your antivirus will definetely flag this as a "CRCK_KEYGEN" or "Hacktool:Win32/Keygen" or something similar, so make sure to turn it off when running, and keep the loader in a safe place. Secondly, if KB971033 windows update is installed, delete that update. It will make Windows Loader not work. Alright, not that is out of the way, let me explain this.

Microsoft has 3 different distribution channels for their products, namely retail, OEM, and volume license. AutoKMSes use the volume license to activate the product, but Windows Vista, and Windows 7 Home Premium/Ultimate only had retail and OEM licenses availible. This means that any autoKMS will not be able to use a volume license to connect to a KMS server to activate the product, because there isn't volume license to begin with. 

This is where Windows Loader by Daz comes in. It injects a System Licensed Internal Code into the system before Windows boots, which will result in Windows thinking it is running on an OEM computer with a license tied to the motherboard. That is, of course, assuming the disk is MBR-partitioned. Also note that all key parts of the loader are encrypted with a custom encryption, and every user has a unique version of the loader installed on his or her system.

![](../main/ReadMe-Reference-Images/Windows-Loader-preview.jpg)

  3) Hwidgen
  
See one of [Aiowares forum pages](https://www.aiowares.com/showthread.php?tid=246) for the source. When downloading, use the link supplied in "Mirror 1" as of December 5th, 2020. Registration is needed.

The Digital License system that Microsoft implements uses hardware based IDs which are unique for each machine. The legit tickets used for the process(can be an Upgrade from a supported predecessor or by using a Win 7/8.1 key) do not contain any product key related info. Hwidgen generates a hardware ID-bound license for your machine based on the hardware ID your machine has according to the same algorithm Microsoft uses to generate your hardware ID. It then installs this license on the machine.

This generated new license is stored in Microsoft's servers and will activate a machine that used Hwidgen even if you do a fresh install of Windows afterwards. Hwidgen only needs to be used once per machine(run once and delete). In later fresh installments of Windows, just skip any key prompts(choose 'I have no product key' during setup) and when the machine makes online contact with Microsoft's servers, they will regocnize the hardware ID and grant activation automatically. Only hardware changes will cause the license generated by Hwidgen being invalidated, but as we all know, this is normal, as *even* **legit** licenses can be invalidated by hardware changes. 

![](../main/ReadMe-Reference-Images/HWIDGEN-preview.jpg)

  4) Raw keys
  
Yep, as its name suggests, they are just activation keys supplied in .txt files. I've surfed the internet, far and wide to find them, and I've confirmed that they all work as of December 5th, 2020. I can't say for sure in the future, though. Use then while you can 😋.

![](../main/ReadMe-Reference-Images/Raw-keys-preview.jpg)

# Closing...
Have fun with your activated software testing for *educational purposes* in *virtual machines* 😛!
