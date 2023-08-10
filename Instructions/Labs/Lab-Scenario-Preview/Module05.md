# Lab Scenario Preview: Lab-05: Explore Azure Network Security Groups (NSGs).

## Lab overview

In this lab, you will explore the function of network security groups in Azure. You will do this by create the VM without any network security group (NSG). Without any NSG to filter traffic, all the ports in the VM are exposed to the public internet. You will then go through the process of creating an NSG and assigning the VM's interface to that NSG. Once configured you will test the connection to the VM, using the default NSG rules and also rules that you will create.

## Objectives

After completing this lab, you will be able to:

- Create a Windows 10 virtual machine
- Create a network security group and assign the network interface of the VM to that NSG.nd create a new inbound rule for RDP traffic
- Test the newly created inbound NSG rule to confirm that you can establish a remote desktop (RDP) connection to the VM
- Allow outbound internet traffic to validate that you can connect to the internet

## Architecture Diagram

 ![](./Images/preview05.png)

Once you understand the lab's content, you can start the Hands-on Lab by clicking the **Launch** button located in the top right corner. This will lead you to the lab environment and guide. You can also preview the full lab guide [here](https://experience.cloudlabs.ai/#/labguidepreview/f4ba658e-0401-499f-9c66-a91afd5f5110) if you want to go through a detailed guide prior to launching the lab environment. 
