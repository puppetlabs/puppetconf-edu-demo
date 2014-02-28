# Virtual Machine Setup

Depending on whether you're using VMware or VirtualBox virtualization software, you will follow slightly 

## VMware

1. Be sure you have an up-to-date installation of your VMware virtualization software.

2. From the VMWare __File__ menu, select __Open__ and navigate to the .vmx file included in your Learning VM download. You can also drag and drop the .vmx file into the VMWare virtual machine library.

3. Don't launch the VM just yet; we'll want to adjust a couple of settings first. With the Learning VM selected in the VMWare library, open the __Settings__ panel and click the __Network Adapter__ icon.

4. Select __Autodetect__ under the __Bridged Networking__ heading as shown in the example.

	![image](../assets/vmware_network_bridged.png)

5. Next, we'll want to allocate some extra memory to the Virtual Machine to ensure that it has the resources neccessary for everything to run smoothly. Go back to __Settings__ panel and click the __Processors & Memory__ icon. We suggest allocating at least two gigabytes of memory. Use the slider to set your memory allocation. Note that the Learning VM will likely still function with less memory allocated, but you may encounter performance issues.

	![image](../assets/vmware_memory.png)

6. Now that your settings are configured, click the __Power On__ button to boot up the VM.

	NOTE: Virtualization software uses mouse and keyboard capture to 'own' these devices communicate input to the guest operating system. The keystroke to release the mouse and keyboard will be displayed at the top right of the VM window.

7. Once the VM is booted up, make a note of the IP address. You'll need this to access your Quest Guide and the Puppet Enterprise Console. If you forget the IP or if it changes, you can access it again by entering the following command in the VM commandline.

		ifconfig

### Let's now get started with the [Weclome Guide](http://something)

<!-- Not needed

8. Now that the VM is running you're ready to launch your Quest Guide. First, Navigate into the quest_guide directory in your virtual machine:

		cd ~/quest_guide
	
9. We built the Quest Guide with a static site generator called Jekyll. To launch the Quest Guide, enter the following command:

		jekyll serve --detach
	
10. To view the Quest Guide, open a web browser on your host system and enter the url, inserting the VM IP you noted earlier:

		<vm's IP>:4000

-->

## VirtualBox

Be sure you have an up-to-date installation of VirtualBox. The Learning VM works best with VirtualBox 4.x. You can find a free download of the latest version at https://www.virtualbox.org/wiki/Downloads.

Choose “Import Appliance” from the File menu and select the .ovf file included with your download.
	
NOTE: __Do not__ use the “New Virtual Machine Wizard” and select the included .vmdk file as the disk; machines created this way will kernel panic during boot. 

Don't launch the VM just yet; we'll want to adjust a couple of settings first. In the VirtualBox Manager panel, select __Network__ to access networking options. Choose __Bridged Adapter__ from the drop-down menu.

![image](../assets/vbox_network_bridged.png)

1. For everything to work smoothly, we suggest allocating at least two gigabytes of memory to the VM. In the VirtualBox Manager panel, click __System__ to access system options and use the slider to set your memory allocation. Note that the Learning VM will likely still function with less memory allocated, but you may encounter performance issues.
![image](../assets/vbox_memory.png)

2. Now that everything is configured, click the __Start__ button in the upper left to boot up the VM.

	Note: Refer to [VirtualBox documentation](http://www.virtualbox.org/manual) for additional information as required.

3. Once the VM is booted up, make a note of the IP address. You'll need this to access your Quest Guide and the Puppet Enterprise Console. If you forget the IP or if it changes, you can access it again by entering the following command in the VM commandline. 

		ifconfig

### Let's now get started with the [Weclome Guide](http://something)

<!-- Not needed

4. Now that the VM is running you're ready to launch your Quest Guide. First, Navigate into the quest_guide directory:

		cd quest_guide

	Note: Virtualization software uses mouse and keyboard capture to 'own' these devices communicate input to the guest operating system. The keystroke to release the mouse and keyboard will be displayed at the bottom right of the VM window.

5. We built the Quest Guide with a static site generator called Jekyll. To launch the Quest Guide, enter the following command:

		jekyll serve --detach
	
6. To view the Quest Guide, open a web browser on your host system and enter the url, inserting the VM IP you noted earlier:

		<vm's IP>:4000

-->