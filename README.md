### UiPath RPA Challenge
# Image Background Remover Bot

[![GitHub](https://badgen.net/badge/icon/GitHub?icon=github&color=black&label)](https://github.com/MaxineXiong)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform - UiPath RPA](https://img.shields.io/badge/Platform-UiPath_RPA-fa4616)](https://www.uipath.com)

<br/>

This repository hosts an automation solution designed to address the challenge outlined in the requirements below.

### **Objective**

Build a bot which **loops through photos in a folder then removes the background of the image using an online AI tool** https://www.remove.bg/. The **new photos must then be saved in a separate folder**. You can download some sample photos in the resources section of this lecture, the file is called "before.zip".

### **Instructions**

- Create a before and after folder in your project's folder. Populate the before folder with the images in the attached zip file.
- Open the browser with an *Open Browser* activity and maximise the browser window with a *Maximise Window* activity.
- Create a FileList variable of type Object Array and assign its value to the "Before" directory files.
- Use a *For Each* activity to loop through each file i.e. object in the object array.
- Click the Upload Image button in the browser. The *Click* activity must be within the body of the For Each loop. Tweak the selector accordingly.
- Use an *Attach Window* activity to attach to the Save As window.
- In the 'File name' field, use a *Type Into* to type the full path of the file then use a *Click* activity to click the 'Open' button. Ensure these activities happen in the background.
- Add a *Click* activity outside and after the *Attach Window* activity to download the file to your downloads folder on your PC.
- Use a *Move File* activity to move the downloaded image from your downloads file to the 'After' folder. Note these folder and file paths will need to be dynamic, so use string manipulation where necessary.
- Ensure that the *Move File* activity won't start until the file is confirmed to have been downloaded. You can use a static delay of 5 seconds for this and add that after the download *Click* and before the *Move File* activity. However, if you're up for the challenge try create a dynamic wait by using these four activities; *While*, *Path Exists*, *Assign* and *If*.
- Use a *Click* activity to click on the x which will remove the uploaded file in the browser after each run. Add this click after the Move File activity.
- Close the browser using a *Close Application* activity.

_You can check out the **automation demo video for the solution** below_:

https://github.com/MaxineXiong/Image-Background-Remover-Bot-RPA/assets/55864839/1579df74-9563-49fd-9ce6-86bf2d0d5e4b









<br/>


## **Installation**

Before installing **UiPath Softwares**, please make sure your system meets the hardware and software requirements outlined in the **[UiPath documentation](https://docs.uipath.com/studio/standalone/2022.10/user-guide/hardware-and-software-requirements)**.

The **Uipath Platform** includes the following tools:

- **UiPath Studio**
- **UiPath Assistant**
- **UiPath Automation Cloud, including UiPath Orchestrator**

<details>  
<summary> To run this project successfully, please follow these steps to install UiPath Studio:
</summary>

***

Step 1 : Visit [uipath.com](https://www.uipath.com/) and click **Try UiPath Free** button.
<p align="center">
<img width="900" src="https://github.com/YenLinWu/RPA_UiPath/blob/master/Installation/README_Images/Install_UiPath_Studio_1.png">
</p>

Step 2: **Sign up** for a personal account.
<p align="center">
<img width="900" src="https://github.com/YenLinWu/RPA_UiPath/blob/master/Installation/README_Images/Install_UiPath_Studio_2.png">
</p>  

Step 3: **Verify** your account in email.
<p align="center">
<img width="900" src="https://github.com/YenLinWu/RPA_UiPath/blob/master/Installation/README_Images/Install_UiPath_Studio_3.png">
</p>  

Step 4: **Log into** the **UiPath Automation Cloud** using your account, and click the **Download Uipath Studio** button.
<p align="center">
<img width="900" src="https://github.com/YenLinWu/RPA_UiPath/blob/master/Installation/README_Images/Install_UiPath_Studio_4.png">
</p>   

Step 5: Click **Sign in**.
<p align="center">
<img width="900" src="https://github.com/YenLinWu/RPA_UiPath/blob/master/Installation/README_Images/Install_UiPath_Studio_5.png">
</p>    

Step 6: Select **UiPath Studio Pro**.
<p align="center">
<img width="900" src="https://github.com/YenLinWu/RPA_UiPath/blob/master/Installation/README_Images/Install_UiPath_Studio_6.png">
</p>  

Step 7: Follow the system instructions to complete the installation of **UiPath Studio Pro**.
<p align="center">
<img width="900" src="https://github.com/YenLinWu/RPA_UiPath/blob/master/Installation/README_Images/Install_UiPath_Studio_7.png">
</p> 

</details> 

<br/>

## **Usage**

To run the RPA workflow on your local machine, follow these steps:

1. Either **download** this repository to your local machine or **clone** it directly within your UiPath Studio.
2. Open the **UiPath Studio** software on your machine.
3. Locate and **open** the **Main.xaml** file from the downloaded repository in **UiPath Studio**.
4. **Run** the **Main.xaml** file to start the RPA process.

<br/>

## **Acknowledgement**

I would like to express my gratitude to the **[UiPath community](https://community.uipath.com/)** for providing resources, tutorials, and a platform for automation enthusiasts to learn and collaborate.

<br/>

## **License**

This project is licensed under the [MIT License](https://choosealicense.com/licenses/mit/), which means you're free to modify, distribute, and use the code in your own projects.
