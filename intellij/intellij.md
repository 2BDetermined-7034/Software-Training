# IntelliJ
This is our preferred java IDE for writing robot code due to its superior java integration. You are more than welcome to continue using vscode, as each editor has its own ups and downs and it is entirely up to personal preference.
If you choose to make the switch, it shouldn't be too hard to figure out how to use it to edit robot projects, though there are a few gradle settings you need to configure before you can deploy code through inteliJ

### Cloning a Repo
![image](https://github.com/2BDetermined-7034/Software-Training/assets/33676445/ee1f49c1-6d7a-4e62-90c2-7a1fdc5d8a25)
The easiest way to clone a repo through the IntelliJ GUI is with the "Get From VCS" button. From there simply copy the url of the git repo and choose a place to save the project, preferrably under 'C:/users/wlhsf/Documents/20XX/Project Name'
Take care not to save projects under a path with Onedrive in it, as this will mess with the build files of your project.

### Installing the FRC extension
![image](https://github.com/2BDetermined-7034/Software-Training/assets/33676445/39b318a7-e37e-4268-b314-d2a00771e48c)
press 'Ctrl+Alt+s' and navigate to "Plugins" to install the FRC extension for IntelliJ if it is not already installed

### Deploying code to the Rio
![image](https://github.com/2BDetermined-7034/Software-Training/assets/33676445/2aee3ab9-ce96-4a86-9cf5-6fb10cd4449e)
Near the top right corner you should see a button labelled "Current File", or something like "build", "deploy", "clean", etc.
If you see the word deploy, simply select it from the drop down and press the green play button while connected to the robot to deploy. 

Otherwise click the dropdown and select "edit configurations"
![image](https://github.com/2BDetermined-7034/Software-Training/assets/33676445/9e317892-63c3-4e06-9ddc-9c09b2b04122)
Click "Add new" and select "Gradle"

![image](https://github.com/2BDetermined-7034/Software-Training/assets/33676445/ff9188f5-f3c8-43e1-8f25-b0866c3bada5)
This menu lets you create gradle shortcuts using gradle commands. To create the configuration for deploying code, type "build deploy" in the "Run" field. 
The "build" keyword compiles your robot project
The "deploy" keyword sends your robot project to the roborio if your laptop is on the robot's wifi or connected via usb-b/ethernet and the rio is detected.

Finally click "apply", close the menu, select your new configuration, and then click the green play button. 
