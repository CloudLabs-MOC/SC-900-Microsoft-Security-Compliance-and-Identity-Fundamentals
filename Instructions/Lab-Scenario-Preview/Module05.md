# Lab Scenario Preview: Lab-05: Explore Azure Network Security Groups (NSGs).

## Lab overview

In this lab, you will explore the function of network security groups in Azure. You will do this by create the VM without any network security group (NSG). Without any NSG to filter traffic, all the ports in the VM are exposed to the public internet. You will then go through the process of creating an NSG and assigning the VM's interface to that NSG. Once configured you will test the connection to the VM, using the default NSG rules and also rules that you will create.

## Objectives

After completing this lab, you will be able to:

- You will create a Windows 10 virtual machine.

- Create a network security group and assign the network interface of the VM to that NSG.nd create a new inbound rule for RDP traffic.

- You will test the newly created inbound NSG rule to confirm that you can establish a remote desktop (RDP) connection to the VM.  Once inside the VM you'll work check outbound connectivity to the internet from the VM.  

- The default outbound rules for NSG allow outbound internet traffic so you will validate that you can connect to the internet. In this You will then go through the process of creating a custom outbound rule to block outgoing internet traffic and test that rule. 

## Architecture Diagram

![](../images/.png)

Now that you know what the lab is going to be all about, you can launch next item **Hands-on Lab** which includes lab environment and lab guide. You can also preview the full lab guide [here](https://experience.cloudlabs.ai/#/labguidepreview/f4ba658e-0401-499f-9c66-a91afd5f5110) if you want to go through detailed guide prior to launching lab environment.  