# SimplyTemplate

Phishing Template Generation Made Easy. The goal of this project was to hopefully speed up Phishing 
Template Gen as well as an easy way to ensure accuracy of your templates. Currently my standard Method
of delivering emails is the Spear Phish in Cobalt strike so you will see proper settings for that by default. 


Current Platforms Supported:
* Kali Linux 2.0
* Kali Linux 1.0

Work Conducted by:
----------------------------------------------
* Alexander Rymdeko-Harvey [Twitter] @Killswitch-GUI -- [Web] [CyberSydicates.com](http://cybersyndicates.com)
* Keelyn Roberts [Twitter] @real_slacker007 -- [Web] [CyberSydicates.com](http://cybersyndicates.com)

A few small benefits:
- Easy for you to write modules (All you need is 1 required Class option and you're up and running)
- Simple intergration of Email Templates
- Also the ability to change major settings fast without diving into the code (Coming)

## Understanding Module Types
All templates will provide you with a small meta tag. This tag will help you quickly identify the 
capabilities of the module, also what the "content" supports.

Sophistication Levels:
- High= Requires proper OSINT / SE to build and effectively deploy the template. These are generally internal based templates with specific themes.
- Medium= Requires a decent amount of modifications or settings, and are more general of a template external based template.
- Low= Requires little to no modifications of the template and are generally not effective.

Core Options:
- Text= Text based option or output.
- Html= Rich Html Supported for output (generally multipart Email Html/Text).
- Link= Template supports a major link for stats or potential web download of document/Drive-by.
- Attachment= Can support text that tells users to open or use the supplied attachment.

## Get Started
Please RUN the simple Setup Bash script!!!
```Bash
root@kali:~/Desktop/SimplyTemplate# sh Setup.sh
or
root@kali:~/Desktop/Simplytemplate# ./Setup.sh
```
## Standard Commands
```
 [>] help
  Availiable Commands:
  -----------------------------------------
  [use]     Select a template for use
  [list]    List loaded Templates
  [info]    Display metadata about a module
  [update]  Update SimplyTemplate from Github
  [help]    Display this menu
  [exit]    Exit SimplyTemplate

  Availiable Template Commands:
  -----------------------------------------
  [set]     Set a option for the Template
  [info]    Info about loaded Templates
  [gen]     Generate Template
  [view]    View Sample Template
  [back]    Go back to main Menu
  [exit]    Exit SimplyTemplate
 [>] 
```

## Standard Startup
```
 ============================================================
 Current: v0.1 | SimplyTemplate | [Web]: CyberSyndicates.com
 ============================================================
   [Twitter]: @real_slacker007 | [Twitter]: @Killswitch_gui
 ============================================================
 Main Selection Menu

  2 Email Template Loaded

 Commands:

  [use]   Select a template for use
  [list]    List loaded Templates
  [info]    Display metadata about a module
  [update]  Update SimplyTemplate from Github
  [help]    Display this menu
  [exit]    Exit SimplyTemplate
 [>] 
```
## List Modules
```
 ============================================================
 Current: v0.1 | SimplyTemplate | [Web]: CyberSyndicates.com
 ============================================================
   [Twitter]: @real_slacker007 | [Twitter]: @Killswitch_gui
 ============================================================
 [*] Available Modules are:

  1)  Modules/CyberNews.py    
  2)  Modules/LinkedinGroup.py

 [>] list
```
## Use a module
```
 [>] use 2

 ============================================================
 Current: v0.1 | SimplyTemplate | [Web]: CyberSyndicates.com
 ============================================================
   [Twitter]: @real_slacker007 | [Twitter]: @Killswitch_gui
 ============================================================

 Template Loaded: Linkedin Group Invite



 Template Required Options:

 Setting      Value Set   Description of Setting
 -------      ---------   ----------------------
 FromFirstName    Jim         Contacts First Name
 FromFullName     Jim Bob     Contacts Full Name
 FromOrg          Veris Group, LLC    Contacts Company
 FromProfileUrl   http://k.com    Linkedin Full Profile URL
 FromTitle        CEO, ATD    Contacts Full Title
 GroupName        Cyber Cyber Cyber   Requested Group to Join
 GroupUrl         %URL%       Custom GroupURL or CS URL
 ProfilePic       http://pic.com    Custom GroupURL or CS URL

 Availiable Template Commands:

  Command   Description
  -------   -----------
  [set]   Set a option for the Template
  [info]    Info about loaded Templates
  [gen]   Generate Template
  [view]    View Sample Template
  [back]    Go back to main Menu
  [exit]    Exit SimplyTemplate
 [>]
 ```
## Simply Use Set and Gen
```
 ============================================================
 Current: v0.1 | SimplyTemplate | [Web]: CyberSyndicates.com
 ============================================================
   [Twitter]: @real_slacker007 | [Twitter]: @Killswitch_gui
 ============================================================

 Template Information:

  Name:                   Linkedin Group Invite
  Author                  Killswitch-GUI
  Sophistication:         Medium
  SampleImage:            Modules/Sample/LinkedinGroup.png
  Info:                   Linkedin uses a very common setup for group and
                          user invites. This template
                          takes advantage of this and uses the Rich HTML
                          from a real email. Places your data
                          into the template and generates a Html/Text
                          Template for you.

 Template Required Options:

 Setting    Value Set   Description of Setting
 -------    ---------   ----------------------
 FromFirstName    Jim         Contacts First Name
 FromFullName     Jim Bob     Contacts Full Name
 FromOrg          Veris Group, LLC    Contacts Company
 FromProfileUrl   http://k.com    Linkedin Full Profile URL
 FromTitle        CEO, ATD    Contacts Full Title
 GroupName        Cyber Cyber Cyber   Requested Group to Join
 GroupUrl         %URL%       Custom GroupURL or CS URL
 ProfilePic       http://pic.com    Custom GroupURL or CS URL
 [>] set FromOrg James Brown, LLC
 [>] gen
```