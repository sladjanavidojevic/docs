# Getting Started

This section introduces you to the main features of Zerynth and provides you a step-by-step guide to get started with the system. Take a look at the video below to see Zerynth in action!

<iframe width="560" height="315" src="https://www.youtube.com/embed/u2pEH5dSZbo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Create a Zerynth User Account

It is necessary to create a User Account to access Zerynth.

To register a new Zerynth Account or to Log in an existing one, you can proceed manually (**email**, **username** and **password**) or you can automatically register/login with social credentials (**Facebook** and **Google+**).

[![](https://www.zerynth.com/wp-content/uploads/2020/03/1_zerynth_login.png)](https://www.zerynth.com/wp-content/uploads/2020/03/1_zerynth_login.png "1_zerynth_login")

## Note

For Manual Registration: check your email and verify your new account by clicking on the link provided in the confirmation email

## Warning

The first time you create a user account or if you have sign-in issues, a restart of Zerynth Studio might be necessary

### Connect, Register and Virtualize your Device

To make a device usable with Zerynth, you need to **Connect**, **Register**, and **“Virtualize”** it.

According to the platform used and to the connected device, the user has to install the related driver to make the machine able to recognize and exchange data with the board.

## Warning

Procedure to install drivers, if needed, is reported device by device in [Supported Devices](https://docs.zerynth.com/latest/supported_boards.html#doc-supported-boards).

The **Registration** phase is the process of retrieving the device info to allow the Zerynth backend to build its specific virtual machine.

![](https://www.zerynth.com/wp-content/uploads/2020/03/2_zredeem.png "2_zredeem")

If the device has never been connected before, by clicking the “Z” button, the registration dialog, shown above, is displayed.

To register a new device, you can follow these steps:

1.  connect your device to the machine. The “Devices Management Widget” notifies the devices list update with a yellow blink;
2.  select the device from the dropdown menu;
3.  click on the “Zerynth” button. Zerynth Studio will guide you in the entire process through info messages displayed in the log console section at the bottom of the screen.

## Note

“Powered by Zerynth” devices are accompained by a redeemable code that can be inserted in the above window and exchanged for a free virtual machine license.

## Warning

Some devices require to be set in Device Firmware Update (DFU) mode in order to allow their registration and the flashing of the Zerynth Virtual Machine. Detailed guides on how to put them in DFU mode is available in the [Supported Devices](https://docs.zerynth.com/latest/supported_boards.html#doc-supported-boards) section of the documentation.

Once registration has been performed, the user is given the option to create a Virtual Machine for the registered device by clicking again the “Z” button.

![](https://www.zerynth.com/wp-content/uploads/2020/03/3_virtualize.png "3_virtualize")

## Note

A device can always be registered again with the dedicated dialog button.

In the figure below, after clicking the “Create” button, the user can select one available of different virtual machines compatible with the target device choosing the licenses (Starter/Premium), the real time operating system from those supported for the target device, and (for Premium licenses only) the features to be included in the virtual machine (FOTA, Power Saving, Secure Firmware, etc.).

![](https://www.zerynth.com/wp-content/uploads/2020/03/4_create_vm.png "4_create_vm")

## Note

Some devices cannot be recognized automatically; for these devices, the dialog provides some more options to be specified before the actual registration/virtualization can take place.

## Warning

The “Available” column in the table shows the possibility to create the related virtual machine according to the user asset.

The created Virtual Machine can now be virtualized (i.e. burned on the device). The **“Virtualization”** is the process of installing the Zerynth Virtual Machine by flashing it on a device. By clicking the “Virtualize” button, the user can select the Zerynth Virtual Machine to be installed in his device choosing from those created.

![](https://www.zerynth.com/wp-content/uploads/2020/03/5_choose_vm.png "5_choose_vm")

## Note

Zerynth Studio toolbar allows to **“Virtualize”** the selected device.

### Zerynth Devices

The supported devices are grouped into Physical Devices (the ones physically connected to the local machine) and Virtual Devices (the devices usable with Zerynth).

The Zerynth “Virtual Devices” feature allows to implement and develop the user application verifying the code for all the supported devices, without having them physically connected to the local machine.

![](https://www.zerynth.com/wp-content/uploads/2020/03/choose-device.gif "choose device")

Once the desired supported device (virtual or physically connected) is selected, Zerynth Studio displays all collected info related to the chosen device in 2 different dialogs:

-   **Device Info Window**;
-   **Device Pinmap Window**.

The **Device Info Window** shows detailed information about the device, including the Flash/Ram size and the port for serial communication.

![](https://www.zerynth.com/wp-content/uploads/2020/03/7_device_info.png "7_device_info")

## Warning

Some boards cannot be automatically recognized by Zerynth Studio and need a disambiguation. In this case the system asks you to indicate the device type. You can always revert this choice by clicking on the “Forget” button.

Finally, the **Device Pinmap window** provides the pinout of the selected device, along with the hardware features and peripherals available on each pin. Thanks to the Device Pinmap window it is also possible to understand how the device embedded peripherals are grouped and/or multiplexed. This allows to better understand how to use each specific hardware feature in the Zerynth Python scripts without having hardware conflicts.

![](https://www.zerynth.com/wp-content/uploads/2020/03/image.png "image")

### Clone an example and start with Zerynth Python Scripts

Zerynth Studio includes many examples to get started: from the most basic ones to the examples related to the installed libraries. Zerynth examples cannot be edited, they are “read only” folders and they can be used as reference for the design of new projects.

Zerynth examples can be cloned in just few clicks:

1.  open the Examples browser by clicking on the “light bulb” icon on the left panel of Zerynth Studio;
2.  select the example you prefer and clone it by clicking on the dedicated button;
3.  At this stage Zerynth converts the example into a new project giving you the possibility to edit the **Title**, the **Description** and the **Folder** of your new project project;
4.  click on “Create” and you are done!

![](https://www.zerynth.com/wp-content/uploads/2020/03/9_clone_example.png "9_clone_example")

## Warning

Remember that Zerynth does not allow two projects to have the same **Folder**

### Verify and Uplink a Zerynth Project

The buttons on the upper left toolbar allow you to verify and uplink a script into a device. To verify a project click on the **Verify** icon to check your script for errors. The errors will be reported in the console and in the code editor with helpful tooltips.

To Uplink your verified project into a Virtualized device just click the **Uplink** icon and follow the Zerynth Studio messages.

![](https://www.zerynth.com/wp-content/uploads/2020/03/uplink_photon.jpg "uplink_photon")

## Warning

Some devices require to be reset during the uplink operation in order to write in flash the bytecode

### Develop your First Zerynth Project

To create your First Zerynth Project from scratch you have to do just a few steps:

1.  click on the button “Browse Project”;
2.  click on “New Project”;
3.  Decide a project title and the project folder, and write an optional description;
4.  click on the “Create” button.

Once you click on the “Create” button, the new Zerynth Project opens and you will be prompted with the editor of the “main.py” file. The main is where the principal Zerynth code is written in Python: here is where you develop the logic of your script.

![](https://www.zerynth.com/wp-content/uploads/2020/03/11_create_project.png "11_create_project")

If you wish to add more files to the Zerynth project you can easily do it. In Zerynth you can create html, json, txt, bin files and save them together with the bytecode on the device flash memory. You can also create more .py files where you can develop other parts of your code like modules and functions to be used in the main.py file.

To add new files to a Zerynth project, follow these steps:

-   click on “Browse Project”;
-   click on “Add file” ;
-   after naming the file click on “Create”;
-   write the code within the empty field in the editor;

You can also add a new folder, delete a selected file, refresh the project folder, etc. by clicking the icon on the right of the “Project view” bar.

![](https://www.zerynth.com/wp-content/uploads/2020/03/12_project_action.png "12_project_action")

## Note

When you add a `.py` file containing some code to be used in the main.py file (e.g. a file named `helpers.py`), you have to import it by adding the line `import helpers` in the main.py file. Thus, you can call functions located in the `helpers.py` file by using the following syntax:

helpers.fun_name(fun_attribute1, fun_attribute2, ...)

## Note

If you want to save the `template.html` in the device flash as resource to be used by a specific module like the Zerynth App library, you have to use the `new_resource()` function defining the following code in the `main.py` file:

new_resource("template.html")

### Import a Zerynth Package into a Project

Packages import syntax is very simple:

-   Official Packages are imported with: `from c import m` where **c** is the name of the package and **m** is the name of a module inside the package. (e.g. `from cc3000 import cc3000` or `from cc3000 import cc3000_tiny`).
-   Community Packages are imported with: `from community.b.c import m` where **b** is the namespace of the package, **c** is the package name and **m** is the name of a module (e.g. `from community.floyd.rtttl import rtttl`)

The import autocomplete feature of Zerynth Studio makes the task of importing modules even easier: as soon as “from” or “import” is typed in the code editor, the autocomplete box lists all the matching modules.

The [Zerynth Programming Guide](https://docs.zerynth.com/latest/official/core.zerynth.stdlib/docs/index.html#zerynthprog) and various programming examples are also provided.

For both the Official Library and the Community Library, a complete documentation is available and if the package contains usage examples, they can be found under the examples tab.

Finally, if you need help with Python, here you can find a good [overview on Python 3](http://en.wikibooks.org/wiki/Non-Programmer%27s_Tutorial_for_Python_3/Print_version#3._Hello.2C_World) with simple and exhaustive examples.

You can always post your questions and doubts on the [Zerynth Community Forum](http://community.zerynth.com/) logging-in with your Zerynth Account.

### Zerynth Studio updates

Zerynth Studio has two different update mechanisms:

-   major system release
-   rolling updates

When a new major version of Zerynth is released a notification “System Update!” will appear in the footer area of Zerynth Studio. By clicking the notification, the new version will be downloaded and installed. After a restart, the new version will be selected and launched. However, the previous version is still there and can be selected during the launch phase. If a previous version is not needed anymore, it can be deleted from the “Preferences” menu.

![](https://www.zerynth.com/wp-content/uploads/2020/03/Zerynth_Studio_Update_Message.jpg "Zerynth_Studio_Update_Message")

On the contrary, rolling updates do not change the system version but just a group of packages. Rolling updates are notified by the “Rolling update” label in the footer area of Zerynth Studio. By clicking the notification, the list of updated packages and a detailed changelog are displayed. If accepted, a rolling update will download the selected packages only and will unpack them. After a restart, the launcher will take care of finishing the update and start Zerynth Studio.

![](https://www.zerynth.com/wp-content/uploads/2020/03/Zerynth_Studio_Update_Rolling.jpg "Zerynth_Studio_Update_Rolling")

### Zerynth and Git

Zerynth Studio offers the possibility to store your projects on our backend, in a private git repository. Such feature is accessible from the Project View in the left panel by clicking the git “code-branch” icon.

![](https://www.zerynth.com/wp-content/uploads/2020/03/15_zstudio_git.png "15_zstudio_git")

The first time a project is pushed to our backend, the “Create repository” option must be selected. From there on, the project view changes, showing a footer with information about the current remote/branch, the current tag if present, the number of modified files (identified by a bullet) and the status of the local repository with respect to the remote repository.

The project git repository is automatically configured with a remote called “zerynth” pointing to our backend. All git operations accessible from Zerynth Studio will operate on that remote. It is however possible to manually configure the project local repository to use different remotes (for example GitHub or GitLab). However, such configuration is up to the user.

Git operations not featured in Zerynth Studio (for example “merge”), can be performed manually using git from the command line.

### Search and Install Community Libraries

Zerynth allows searching and installing libraries created by Zerynth users and hosted on GitHub.

Libraries can be searched and installed from the Zerynth Library Manager Section (“puzzle” icon) in the left toolbar. The latest version is displayed and options to update or downgrade the library are present.

The results of the search are shown in the left column that displays a brief description of the libraries together with the available version. By clicking “Install” or “Update” the library can be easily added to the system.

![](https://www.zerynth.com/wp-content/uploads/2020/03/16_search_install_package.png "16_search_install_package")

### Publishing community libraries

Zerynth Studio allows publishing your projects as community libraries that can be installed by everyone else in the Zerynth community. To publish a project, select the “Publish” option for the currently opened project to fire up the publish wizard.

The first step is needed to get the user permission to manage the Github repository where the library will be hosted. In order to do so, a popup window will be displayed and the Github authorization flow for Zerynth will be started. It is usually needed to login to Github with the user credentials and authorize Zerynth. Upon correct authorization the Zerynth backend will associate the Github account with the user Zerynth account.

![](https://www.zerynth.com/wp-content/uploads/2020/03/zstudio-publish-0.png "zstudio-publish-0")

In the second step the Github repository to host the library on must be chosen from the available ones. Some information on the library must be given in this step, namely:

-   the library title: will be displayed in the Library Manager
-   the library description: a short text that will be displayed in the Library Manager and that will be indexed to ease searching for libraries
-   a list of keywords to tag the library
-   the version of the library that will be made available after publishing
-   a descriptive text for the version (usually a list of changes, bugfixes and improvements)

If the library has already been published, some of the required field will be automatically filled.

![](https://www.zerynth.com/wp-content/uploads/2020/03/zstudio-publish-1.png "zstudio-publish-1")

The third step is a recap of what is going to happen during the publishing; read it carefully and confirm the repository, the project and the version of the library!

![](https://www.zerynth.com/wp-content/uploads/2020/03/zstudio-publish-2.png "zstudio-publish-2")

In the last step the selected Github repository is cloned, the project to be published is copied in and the changes are committed and pushed back to the master branch. Also, a new Github release is created with version and description given in step 2. As soon as the Zerynth backend discovers the new release, the library will be made available to all the Zerynth users.

## Important

In order for the users of your library to have a better programming experience, we strongly suggest to add examples and documentation. Please refer [here](https://docs.zerynth.com/latest/official/core.zerynth.toolchain/docs/official_core.zerynth.toolchain_packages_packagecmd.html#ztc-cmd-package-publish) for more details.

### Creating Custom Virtual Machines

Zeryth Studio allows creating custom Virtual Machines for PCBs and devices based on supported microcontrollers (At the moment only ESP32 has the support for custom VMs, more architectures will be added soon). The customization process involves editing a template file where many settings like pin mapping and onboard peripherals can be specified. More info can be found [here](https://docs.zerynth.com/latest/official/core.zerynth.studio/docs/index.html#zstudio-custom-vms) and [here](https://docs.zerynth.com/latest/official/core.zerynth.toolchain/docs/official_core.zerynth.toolchain_virtualmachines_vmcmd.html#ztc-cmd-vm-custom).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQyNjk5NzQ2NCw2NDYzNTU2MF19
-->