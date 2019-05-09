.. _upgrade:

------------------------
Upgrade a cluster
------------------------

*The estimated time to complete this lab is 30 minutes.*

Overview
++++++++
This module will show you how you can perform updates of the cluster.
You will perform:

 - NCC upgrade
 - Preparations for a AOS upgrade (Pre-Upgrade)
 - Preparations for a AHV upgrade (Pre-Upgrade)


.. note:: The screenshots that are used are examples of it would might look like. They might not represent the screenshots you will see.


NCC Update
+++++++++++++
The NCC (Nutanix Cluster Checks) are scripts that are performed by the cluster on a scheduled and/or ad-hoc manner
Perform the following steps to run the NCC check:

1. Click on the *Gear* icon to open up the Settings screen.

  .. figure:: images/upgrade-01.png

2. Select the *Upgrade Software* tab on the left side of the screen

  .. figure:: images/upgrade-02.png

3. Select the *NCC* tab and see if the current version and the available version
4. If there is a version available, click on the Download button so the cluster can download the version.
5. In the *warning* screen, click the **Yes** button. This will start the download.

  .. figure:: images/upgrade-04.png

  .. figure:: images/upgrade-05.png

6. In the top bar of PRISM you can also see a blue donut appear. When all is going well that will turn into a green donut after a successful download.

  .. figure:: images/upgrade-06.png

7. After the download has been successful, the *Downloadbar* will turn into a button named *Upgrade*. Click this button and answer the *warning* screen by clicking on the **Yes** button.

  .. figure:: images/upgrade-08.png

8. This will trigger the upgrade process of the NCC. The upgrade process can be followed by clicking on the *Open* text.

  .. figure:: images/upgrade-10.png

9. After everything has been upgrade, **100%**, click on the *Close* text, the **Back to Versions** button and see that the NCC version has changed to the new version.

  .. figure:: images/upgrade-12.png

10. Your Cluster is now running the latest NCC version.

.. raw:: html

  <font color="red"><B>This concludes the NCC upgrade part of this module</B></font>

AOS Pre-upgrade
+++++++++++++++
The AOS (Acropolis Operating System) is Nutanix' CVM (Controller Virtual Machine) system. This AOS will be updated once every while due to a few reasons:

- New features
- Bugfixes
- Support for new hardware

As we have just updated the NCC, updating the AOS is something that is roughly the same from a process steps point of view.
The steps are:

1. Click on the *Gear* icon to open up the Settings screen.
2. Select the *Upgrade Software* tab on the left side of the screen
3. Select the *AOS* tab and see if the current version and the available version

  .. figure:: images/upgrade-13.png

4. Click the **Download** button to start the download of the AOS update. And click on the **Yes** button in the *warning* screen.

  .. note::
    As our cluster is connected to the internet, it can download the AOS files it self. It the cluster is not connected to the internet, due to security reasons as an example, we can use the "darksite" method to upload the file.
    `This article <https://portal.nutanix.com/#/page/docs/details?targetId=Web-Console-Guide-Prism-v51:wc-cluster-nos-upgrade-intro-wc-r.html>`_ describes the process of that.

5. After the download has finished, click the **Upgrade** button and select **Pre-upgrade**. This process will just run checks against the cluster. Click the **Yes** button to start the process.

  .. figure:: images/upgrade-16.png

6. Monitor the *Pre-upgrade* process by clicking on the *Open* text.

  .. figure:: images/upgrade-18.png

7. After the process has reached the 100% marker, the environment is ready to be upgraded. All processes and components needed for the upgrade are ready.

.. raw:: html

  <font color="red"><B>This concludes the AOS pre-upgrade part of this module</B></font>


AHV Pre-upgrade
+++++++++++++++
The AHV (Acropolis Hyper Visor) is Nutanix' Hypervisor. It will be updated once every while due to a few reasons:

- New features which are needed to make some AOS features work. Think about Flow, Buckets and Calm as examples.
- Bugfixes
- Support for new hardware

As we have just updated the AOS, updating the AHV is something that is roughly the same from a process steps point of view.
The steps are:

1. Click on the *Gear* icon to open up the Settings screen.
2. Select the *Upgrade Software* tab on the left side of the screen
3. Select the *AHV* tab and see if the current version and the available version

  .. figure:: images/upgrade-20.png

4. Click the **Download** button to start the download of the AHV update, if not already done. And click on the **Yes** button in the *warning* screen.

  .. note::
    As our cluster is connected to the internet, it can download the AOS files it self. It the cluster is not connected to the internet, due to security reasons as an example, we can use the "darksite" method to upload the file.
    `This article <https://portal.nutanix.com/#/page/docs/details?targetId=Web-Console-Guide-Prism-v51:wc-cluster-nos-upgrade-intro-wc-r.html>`_ describes the process of that.

5. After the download has finished, click the **Upgrade** button and select **Pre-upgrade**. This process will just run checks against the cluster. Click the **Yes** button to start the process.

  .. figure:: images/upgrade-21.png

6. Monitor the *Pre-upgrade* process by clicking on the *Open* text.

7. After the process has reached the 100% marker, the environment is ready to be upgraded. All processes and components needed for the upgrade are ready.

.. note::
  This concludes the Upgrade Module


Takeaways
+++++++++

What are the key things you should know about **Upgrade process**?

- The cluster can be easily upgraded on the following levels:

  1. Firmware of the systems (like BIOS and BMC)
  2. AOS version
  3. Hypervisor version
  4. NCC
  5. Foundation version

- The upgrade has a low impact on the workloads that are running

- Controlled and automated upgrade process where very low human intervention is needed




