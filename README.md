# PracticalSeries Automation Library &mdash; PAL <img height="25px" src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/m1-badge.svg?bxno=d0014A-001-000">

<br />

<p align="left">
    <img width="500px" src="https://practicalseries.com/2001-pal/00-comres/11-resources/02-images/pal-logo-github.svg">
</p>



<table>
    <tr>
        <td align="center"><br><strong>Published by:</strong><br>The PracticalSeries of Publications<br>Published in the United Kingdom<br><a href="https://practicalseries.com">https://practicalseries.com</a><br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;</td>
        <td align="center"><strong>Copyright &copy; 2021</strong><br>Michael Gledhill<br><a href="mailto:mg@practicalseries.com">mg@practicalseries.com</a><br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;</td>    
    </tr>
</table> 

###### A series of technical documents for engineers (and others)
<br />

<table>
    <tr>
        <td colspan="2"><h1>Contents</h1></td>
    </tr>
    <tr>
        <td colspan="2"></td>
    </tr>
    <tr>
        <td align="left"> 
            
[1.&emsp;&emsp;Introducing the PAL](#1--introducing-the-pal)
            
[2.&emsp;&emsp;Revision status](#2--revision-status)<br>
[&emsp;&emsp;&ensp; 2.1. &emsp; &nbsp;Branch revision status](#21branch-revision-status)<br>
[&emsp;&emsp;&ensp; 2.2. &emsp; &nbsp;Previous branches](#22previous-branches)<br>
[&emsp;&emsp;&ensp; 2.3. &emsp; &nbsp;Module Release Status](#23module-release-status)

[3.&emsp;&emsp;Objectives and benefits](#3--objectives-and-benefits)

[4.&emsp;&emsp;An overview of the project](#4--an-overview-of-the-project)<br>
[&emsp;&emsp;&ensp; 4.1. &emsp; &nbsp;Standard modules](#41standard-modules)<br>
[&emsp;&emsp;&ensp; 4.2. &emsp; &nbsp;Application moduless](#42application-modules)<br>
[&emsp;&emsp;&ensp; 4.3. &emsp; &nbsp;Template modules](#43template-modules)<br>
[&emsp;&emsp;&ensp; 4.4. &emsp; &nbsp;Document modules](#44documentation-modules)<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        </td>
        <td align="left">

[5.&emsp;&emsp;Software Control](#5--software-control)<br>
[&emsp;&emsp;&ensp; 5.1. &emsp; &nbsp;Workflow diagram](#51workflow-diagram)<br>
[&emsp;&emsp;&ensp; 5.2. &emsp; &nbsp;Software Control Mechanism](#52software-control-mechanism-general-rules)<br>
[&emsp;&emsp;&ensp; 5.2.1 &emsp;Development branch names](#521-development-branch-names)

[6.&emsp;&emsp;How to use this repository](#6--how-to-use-this-repository)

[7.&emsp;&emsp;Licence](#7--licence)

[8.&emsp;&emsp;Contact the author](#8--contact-the-author)<br>
[&emsp;&emsp;&ensp; 8.1. &emsp; &nbsp;Privacy and personal data](#81privacy-and-personal-data)<br>

[&emsp;&emsp;&ensp; A note by the author](#and-finally-a-note-by-the-author)<br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        </td>    
    </tr>
</table> 

<br />

# 1. &emsp; &nbsp;Introducing the PAL

The Practical Series Automation Library (PAL) is a library of software modules and templates that have been developed for the Siemens Simatic S7-1500 range of controllers (and to a lesser extent the S7-1200 range).

The full library and all necessary documentation is available from the Practical Series website:

&emsp; &emsp; &emsp; [https://practicalseries.com/2001-pal/11-web/index.html](https://practicalseries.com/2001-pal/11-web/index.html)


The PAL is configured and deployed using the Siemens Simatic TIA Portal programming environment.

The PAL software structure is designed such that it is applicable to virtually all industrial applications that can generally controlled by a programmable logic controller.

In general terms, the PAL software being developed as part of this Project, is considered to be suitable for use in the following types of industries (this is not an exhaustive list):

* Water and waste water treatment

* Pharmaceutical and batch production

* Brewing and fermentation

* Chemical manufacturing

* Oil and gas systems

* Food and beverage production

Such applications can generally be thought of as processes that operate with a response time of more than 100 ms. I.e. the system would not be expected to respond to some stimuli faster than 100 ms. In practice, a Controller may (and usually will) respond faster than this; however, a response time of 100 ms is considered to be an acceptable limit for PLC control.

At its most basic level, the PAL will be a library of software modules that control the fundamental aspects of an industrial plant; such modules would for example read the value of an instrument, operate a valve or drive, perform a calculation &c.

Such software modules are referred to as standard modules, these are fixed modules that perform a particular function and are identical across all software installations.

The PAL also contains application specific modules; these contain software that is applicable to the plant being controlled.

The Practical Series Automation Library is freely available under the [MIT Open-Source Licence](#7--licence). Those who find it useful may, if they wish, make a donation to support the library.

Donations can be made here:

&emsp; &emsp; &emsp; [https://practicalseries.com/2001-pal/11-web/81-00-pay.html](https://practicalseries.com/2001-pal/11-web/81-00-pay.html)

The PAL contains fully deployable software that has been developed by the author in his profession as a chartered electrical engineer. It is currently in use on various live plants throughout the UK and in some other parts of the world.

This software is suitable for controlling and automating most industrial applications (typical process applications). It is easy to use and configure, but does have a degree of practical complexity appropriate for the environments within which it is employed. It is heavily configurable, has various operating modes and is suitable for a multitude of industrial applications.

<img src="https://practicalseries.com/2001-pal/31-git/01-pages/00-00-index/02-images/warning.svg?bxno=d0014A-001-000">

<br />

# 2. &emsp; &nbsp;Revision status

All development work takes place on development branches, the always start with a D. Development work is merged back to the master branch when development work is complete and has been tested.

The master branch always contains the most up to date version of the tested and deployable software.

The current revision status of the master branch and any development branches is shown below:

## 2.1.&emsp;&emsp;Branch revision status

| Branch             | Revision                               | Status
| ------------------ | -------------------------------------- | -----------------------------
| <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/m1-name.svg?bxno=d0014A-001-000">           | <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/m1-badge.svg?bxno=d0014A-001-000"> | <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/m1-text.svg?bxno=d0014A-001-000">
| <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/d1-name.svg?bxno=d0014A-001-000">           | <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/d1-badge.svg?bxno=d0014A-001-000"> | <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/d1-text.svg?bxno=d0014A-001-000">
| <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/d2-name.svg?bxno=d0014A-001-000">           | <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/d2-badge.svg?bxno=d0014A-001-000"> | <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/d2-text.svg?bxno=d0014A-001-000">
| <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/d3-name.svg?bxno=d0014A-001-000">           | <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/d3-badge.svg?bxno=d0014A-001-000"> | <img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/02-build/d3-text.svg?bxno=d0014A-001-000">

The full workflow for the project is shown in the [Software Control](#5--software-control) section of this document.

<br />

## 2.2.&emsp;&emsp;Previous branches

|Branch         |Block identifier                    |Details                             |
|---------------|------------------------------------|------------------------------------|
|D0002A-FC18151 |StdSubTimeEventRTC                  |Migration to VCS — Released for use |
|D0005A-FC01001 |StdSysGlobalData                    |Migration to VCS — Released for use |
|D0006A-FC18001 |StdSubScaleAI                       |Migration to VCS — Released for use |
|D0006B-FC02001 |StdInstAnalogRead                   |Migration to VCS — Released for use |
|D0008A-FC11001 |StdDevValveIsol                     |Released for use                    |
|D0009A-FC19512 |StdDebugInst2Order                  |Released for use                    |
|D0010A-UNIFY   |All blocks - standardisation        |All blocks re-release at R002.000   |
<br />

## 2.3.&emsp;&emsp;Module Release Status

|Block     |Name                   |Revision    |Date        |
|----------|-----------------------| -----------| -----------|
|FC01001   |StdSysGlobalData       |002.000     |2022-04-16  |
|FC02001   |StdInstAnalogRead      |002.000     |2022-04-16  |
|FC11001   |StdDevValveIsol        |002.000     |2022-04-16  |
|FC11011   |StdDevValve3Way        |001.000     |2022-06-11  |
|FC18001   |StdSubScaleAI          |002.000     |2022-04-16  |
|FC18151   |StdSubTimeEventRTC     |002.000     |2022-04-16  |
|FC19512   |StdDebugInst2Order     |002.000     |2022-04-16  |
|FC61000   |DocGenExample          |002.000     |2022-04-16  |         




<br />


# 3. &emsp; &nbsp;Objectives and benefits

The object of the Project is to provide a library of standard, validated software modules that can be used within a project without further module testing (the modules having already been validated). 

The only modular level testing of these standard modules would be to confirm that they are identical to the original released PAL modules, and this is easily done with the existing facilities within the Siemens Simatic TIA Portal programming environment.

The benefits of this approach is that subsequent projects that use the Practical Series Automation Library of software modules do not require the extensive design and documentation stages needed to develop software modules in the first place, neither do the modules require testing, nor the documentation needed to test them. This has already been done (and written) as part of this Project and is issued in verifiable form by this Project.

<br />

# 4. &emsp; &nbsp;An overview of the project

The Practical Series Automation Library (PAL) Project is a library of software modules and templates that are to be made available for the Siemens Simatic S7-1500 range of Controllers, it will also work on the S7-1200 range; however, the S7-1200 range has limited capacity compared with the S7-1500, and the full library and all its documentation may not fit in the smaller units.

The PAL is configured and deployed using the Siemens Simatic TIA Portal programming environment.

The library is to be freely available to anyone who wants it under the MIT Open Source licence (see the [LICENCE](LICENCE.md) document).

The PAL software structure is to be designed such that it is applicable to virtually all industrial applications that can generally be controlled by a programmable logic controller (PLC).

At its most basic level, the PAL will be a library of software modules that control the fundamental aspects of an industrial plant; such modules would for example read the value of an instrument, operate a valve or drive, perform a calculation &c.

## 4.1.&emsp;&emsp;Standard modules

Such software modules are referred to as standard modules, these are fixed modules that perform a particular function and are identical across all software installations.

The PAL also contains application specific modules; these contain software that is applicable to the plant being controlled.

For example, if a project were to control five valves, there would be an application module that called the standard valve de-vice driver five times and each instance would link the standard module to the particular IO and internal storage locations associated with the valve in question.

In the context of this Project standard modules are software modules that will carry out a particular function; an example would be a module that controls the operation of a valve, such a module would typically do the following:

* Open and close the valve when commanded to do so

* Determine if the valve is in a fault condition (i.e. the valve did not open when commanded to do so)

* Provide status information about the valve allowing other systems (SCADA, HMI &c.) to display the condition of the valve (i.e. opened, opening, closed, closing, fault, interlocked &c.)

The module would be configurable to accommodate different types of valves and signalling arrangements:

* Different arrangements of position feedback (none, open only, closed only or both open and closed)

* Different opening and closing times

* Handle external fault signals (typical for motorised valves)

* Accommodate different energising states (i.e. energise to open or energise to close)

* Manage different interlock arrangements and signals

The module would also determine how the operator could interface with the valve:

* Provide manual control (operator can take direct control of the valve)

* Restrict specific manual control function (this ranges from full control using simulation to override faults, to no control whatsoever, even restricting the display of faceplate interfaces)

* Allow or restrict the operator from changing operating parameters associated with the valve

The PAL will have many such modules; in fact these modules will make up the bulk of the PAL. 

The standard modules within the PAL will be fixed modules, the software within these modules will be written, tested and validated as part of this Project and at only that point will the modules be released for use. Once released, the modules must not be modified or changed in any unauthorised way, to do so would invalidate the software.

The further modification of any of these standard modules (or indeed the addition of further standard modules) will only take place under the Project change control put in place by this document or under the control of subsequent future projects.

## 4.2.&emsp;&emsp;Application modules

Application modules are specific to each individual plant within which the PAL is deployed; they will be written for a particular project and are configured to match the requirements of that project. 

Although individual in nature, the type of application modules required by a particular project form will be part of a universal set of such modules, typically:

* System (internal) signal generation

* Instrumentation

* Safety and interlock systems

* Calculations

* Continuous control

* Sequence control

* Command execution logic

* Device handling (valves, drives &c.)

* Alarm handling

* Communications

Each application module will also have to conform to the standards, formats and specifications laid out in the various requirements and design documentation associated with the PAL project.

As such, a comprehensive set of template application modules will be designed, developed, tested and issued as part of the Practical Series Automation Library Project.

These modules will serve as an example application (albeit a relatively simple application) to demonstrate how the PAL modules should be used, how they should be documented and the best practices for doing so.

## 4.3.&emsp;&emsp;Template modules

Template modules are example modules that explain how to do things within the PAL, a typical template module being one that shows how sequences work within the PAL. 

Template modules contain a basic configuration that can be copied, expanded and modified for the application in question; they provide a basic “prototype” software structure that can be used repeatedly for a particular type of application.

Template modules exist for each type of application modules and should be used wherever possible as a model for the application module.

Templates are used to help develop the software for a particular plant by providing various examples of how to structure the software.

## 4.4.&emsp;&emsp;Documentation modules

The PAL software is extensively commented (indeed, it has its own Style Guide dedicated to explaining how to comment the PAL software); the documentation modules contain examples of different types of comments for the various different software modules and data structures used within the PAL.

Like the template modules, the documentation modules are used to make the development of the software easier, and provide various examples of how best to implement it.

<br />

# 5. &emsp; &nbsp;Software Control

All software development takes place away from the ```master``` branch on individual development branches. Such development branches have very restricted scope and objectives and once complete (and tested) are merged back to the ```master``` branch. The Software Control Mechanism for this approach is explained below

The full, historic workflow for the project is shown below:

## 5.1.&emsp;&emsp;Workflow diagram

The workflow diagram shows the current state of the repository and identifies all development branches (both past and present) as well as the main ```master``` branch. The workflow diagram(s) lists all the commit points within the repository and the tag identifiers given to each.

<img src="https://practicalseries.com/2001-pal/01-admin/99-0000-git-pal-sw/01-workflow/wf-001p.svg?bxno=d0014A-001-000">
<p align="center"><sup>Workflow diagram</sup></p>



## 5.2.&emsp;&emsp;Software control mechanism (general rules)

A full explanation of the revision mechanism used here, is given in this document:

&emsp; &emsp; &emsp; [https://practicalseries.com/2001-pal/31-git/11-00-scm.html](https://practicalseries.com/2001-pal/31-git/11-00-scm.html)

**The following is a brief summary of the revision mechanism rules:**

The ```master``` branch (after some initial development work to establish it) will only contain software that has been released for use.

>*Released modules are modules that have undergone a software module test (SMT) and have passed that test (i.e. a module that is deployable) — it does not indicate that all software modules are finished, just that the module in question is complete, tested and deployable.*

Individual modules will be developed on a development branch.

When the software as a whole (all modules), has completed module testing, integration testing, has been commissioned and qualified, then the software as a whole will be released for use.

Development work can take place at any time and will always take place on a separate branch. Development branches always spur from some definite commit point on the ```master``` branch.

A development branch must have a very restricted scope. E.g. a single module or group of related modules. 

Generally, a development branch will contain all the things associated with that module (i.e. the function, any data types &c.).

When the module development is complete and tested, it will be merged back to the ```master``` branch, the merge point will be given a five-character tag):

<img src="https://practicalseries.com/2001-pal/31-git/01-pages/00-00-index/02-images/fig-05-01.svg?bxno=d0014A-001-000">
<p align="center"><sup>Fig 05-01 &mdash; A development branch</sup></p>

### 5.2.1&emsp;&emsp; Development branch names

Development work always takes place on a separate ```development``` branch.

A development branch must have a very restricted scope. E.g. a single module or group of related modules. 

Each ```development``` branch is taken from the latest primary commit point on the ```master``` branch (generally referred to as the ```HEAD```). The name given to a ```development``` branch is always in the format:


&emsp; &emsp; &emsp; ```SNNNNb-MMYYYYY```

Where ```SNNNN``` is the commit point tag on the ```master``` branch from which the development branch diverges. 

The ```b``` character is an ordinal character identifying multiple branches that start from the same ```master``` branch commit point, the first branch received character ```A```, the second ```B```, the third ```C``` &c.

The remainder of the branch name refers to the object being developed; these are generally software modules. ```MMYYYYY``` specifies the object under development, for example ```FC01001```. It could equally apply to just a data type e.g. ```UT01000```.

This arrangement can be seen below:

<img src="https://practicalseries.com/2001-pal/31-git/01-pages/00-00-index/02-images/fig-05-02.svg?bxno=d0014A-001-000">
<p align="center"><sup>Fig 05-02 &mdash; Multiple development branches</sup></p>

<br />

# 6. &emsp; &nbsp;How to use this repository

This repository stores the PAL software. This software is written for the S7-1500 range of Siemens Simatic Controllers (what used to be called Programmable Logic Controllers or PLCs).

The software is written using the Siemens programming package TIA Portal, specifically, version 16 of TIA Portal. This version of TIA Portal supports the concept of Workspaces. Workspaces are essentially just Windows folders into which the programmable aspects of a TIA Portal Project (blocks, data types, symbolic tags &c.) can be exported (or imported) as XML files.

This Workspace facility lends itself to the Git (and GitHub) version control systems, they can read and track the changes made to the exported XML files. 

Siemens allow the use of “add-ins” within TIA Portal and these are able to interface with the Workspace and its contents. Siemens have produced their own Git add-in, which allows the Workspace to support and act as, a local Git repository. The add-in also supports the use of **push** and **pull** commands, allowing the local repository to link to this remote repository.

There are two ways to use this repository, firstly as a Workspace connected to any TIA Portal Project you have created. Secondly, the software at each commit point is stored as a complete, archived TIA Portal project (a ```.zap16```) file, and this can simply be retrieved using TIA Portal and will open as a fully populated TIA Portal Project. For those of you familiar with TIA Portal, but not Git, GitHub, or Workspaces, I suggest this second approach. The latest archived project can be found here:

&emsp; &emsp; &emsp; [https://practicalseries.com/2001-pal/31-git/81-00-archive.html](https://practicalseries.com/2001-pal/31-git/81-00-archive.html)

For the more adventurous of you &mdash; those for whom a Workspace is nothing to fear &mdash; follow the summarised instructions below.

>*Note:&emsp;The instructions below are just a summary, a quick reference; there is a more comprehensive explanation here:*

&emsp; &emsp; &emsp; [https://practicalseries.com/2001-pal/31-git/12-00-workspace.html](https://practicalseries.com/2001-pal/31-git/12-00-workspace.html)

To use the Workspace version of the software, do the following: 

1. In TIA Portal, open or create the project you want to use

2. Either add an S7-1500 controller and call it CON100 or rename any existing controller as CON100 (note, this software is compatible with only S7-1200 and S7-1500 controllers)

3. In the Project tree, open the Version Control Interface and add a new Workspace, call it whatever you like and open it in the central window

4. Click the configure **workspace** button (point 1 below):

<p align="center">
    <img width="600px" src="https://practicalseries.com/2001-pal/31-git/01-pages/00-00-index/02-images/fig-06-01.png?bxno=d0014A-001-000">
</p>

5. In the dialogue box enter the location of the folder you want to use in the **Workspace path** field (click the three dots to navigate, or create a folder). Leave the **version control add-in** field blank

6. In this repository, navigate to the latest commit on the ```master``` branch (this will be the default location when you go to the repository page), download the ```CON100``` folder (if its zipped, unzip it and paste the contents into the folder you allocated as the Workspace, it will look like this:

<p align="center">
    <img width="600px" src="https://practicalseries.com/2001-pal/31-git/01-pages/00-00-index/02-images/fig-06-02.png?bxno=d0014A-001-000">
</p>

7. In the Workspace in TIA Portal, copy the ```CON100``` folder from the right-hand side to the left-hand side to update the project

Again, a full explanation is available here:

&emsp; &emsp; &emsp; [https://practicalseries.com/2001-pal/31-git/12-00-workspace.html](https://practicalseries.com/2001-pal/31-git/12-00-workspace.html)

<br />

# 7. &emsp; &nbsp;Licence

The software and all associated documentation is made available under the MIT licence, see the [LICENCE document](LICENCE.md) for full details and an explanation of why I chose this licence.

<br />

# 8. &emsp; &nbsp;Contact the author

My name is Michael Gledhill and I am the author of the software contained within this repository.

You can reach me by email. I invite questions, corrections, constructive criticism and complaints (polite ones) with the following caveats:

1. I do have a day job (surprising isn’t it), I will respond to all polite emails but not necessarily instantly.

2. I can’t offer detailed engineering advice about specific problems (e.g. why does that valve blow all the fuses when I try to open it), but I will offer pearls of wisdom about less specific software issues.

3. I don’t know anything about car engines or kettles so please don’t ask.

4. If your email comes down to *“I think your work is rubbish, I won’t be making any donations, but I do want to shout at you for a while about your outrageous shortcomings”* then please, there is no need to trouble yourself; you’ve already said everything by not paying.

So if you’re happy with that, you can reach me here:

&emsp; &emsp; &emsp; [mg@practicalseries.com](mailto:mg@practicalseries.com)

I’ve included the full details of how I store and manage emails in the privacy and personal data section below:

## 8.1.&emsp;&emsp;Privacy and personal data

This is a big thing now in Europe and in England: [GDPR](https://ico.org.uk/for-organisations/guide-to-the-general-data-protection-regulation-gdpr) *(General Data Protection Regulation)*; it means I have to be very careful with any data I collect about people. I also have to explain why I want the data and what I’m going to do with it. So here goes:

The various websites associated with the work I’ve done here, do not ask for, nor do they collect, any personal data. There is no *contact-me* form that asks for names, addresses, email details or phone numbers &c. Neither are there any user logons or other such forms of identification.

People can email me if they want to, but that is their choice (I gave my email address in the previous section) and I will respond as an individual to any emails I receive.

Where people do email me, I will not pass on any of their details to anyone else *(even when they are rude to me)*. I respond directly to the sender and do not copy, forward or otherwise redistribute their emails with anyone else.

I delete all emails three months after the email conversation is complete (i.e. if you haven’t emailed me for three months, I delete all the emails I’ve received from you and any replies I’ve sent to you). 

I do not reply to abusive emails *(never argue with a stranger on the internet)* and these I delete straight away.

Where someone has asked a common or pertinent question, I may store the question itself and my response (these are copied to an offline Word FAQ sheet — what engineers call a *technical query sheet*), but I do not store any of the questioner’s details (just the question and answer in an anonymous *text based* format).

I also receive the email addresses and some contact details of those people who make a donation. This information is provided to me by [PayPal](https://www.paypal.com/en/webapps/mpp/ua/privacy-full) &mdash; they tell me who has made the donation.

If the donation is for £5 or more, I keep certain information about that individual in a secure offline database. I store precisely:

* Name
* Email address
* Donated amount
* Date of the donation

I do this purely for the purpose of sending those people a link to the downloadable pdf files for various aspects of this project (I make these freely available to all who donate £5 or more).

I keep this information so that I can send a link for each new revision of the pdfs when such revisions are issued (typically once a year). I.e. I make the pdfs available in perpetuity.

I do not share this information with anyone.

I do not send marketing or unsolicited emails of any kind (I do not have a mailing list or anything like that).

Anyone wishing to have their details deleted need only ask. You can contact me at the following email address:

&emsp; &emsp; &emsp; [mg@practicalseries.com](mailto:mg@practicalseries.com)

<br />

# And finally, a note by the author

I’ve written various articles and produced a website that provides detailed instructions for understanding, configuring and programming the Siemens S7-1500 range of controllers (often referred to as *programmable logic controllers* or PLCs).

Those articles and website refer to a library of software modules: the *Practical Series Automation Library* (PAL) &mdash; *the thing contained in this repository* &mdash; that I have developed over several years (I am by profession a chartered electrical engineer, and I programme these controllers for a living). The PAL is fully deployable software that is suitable for the control of most industrial process applications; it is the same software I use in my day job as an engineer. It is currently in use on various live plants throughout the UK and in some other parts of the world. 

This is my software, I developed and tested it, it is my intellectual property and I have made a living charging people money to use it.

Now, while I do not in any way give up my intellectual property rights to this software *(I will continue to develop and modify it in any way that I see fit)*, I am making it available to the you, dear reader, and to the world at large. I’m also going to explain *(in excruciating detail)* how it works, and why, from an engineering perspective, it is configured as it is.

*“Why am I doing this?”* you ask.

Well, it’s partly philanthropy, but it is also the fact that I should have written this stuff down years ago, and now I’ve started, I’m finding the process quite enjoyable and cathartic — and since engineering is a dying profession in England, I’ve decided to share my knowledge with anyone to whom it may be of interest.

I’m also getting old, and before I sink into my dotage and start dribbling into my porridge, I’ve decided to give something back; I’m passing on my knowledge and experience to the next generation of engineers *(if there is one)*.

So you are free to use the software contained herein (you can even download my library of modules without doing any work at all) — yes, it is my software, yes, I own it, but I’m not going to sue anyone who uses it &mdash; *fill your boots* &mdash; I ask only that you are kind enough to credit me in your software (and if you find it useful, to possibly make a donation).

Bear in mind this is proper industrial software and has a degree of practical complexity appropriate for the environments within which it is employed &mdash; this is not the simple *“open a valve and fill a tank”* software you find on PLC training courses &mdash; this is the real thing, it is proper engineering software, written by a proper engineer. *Use it wisely young Skywalker*.

One final point, this is complicated software suitable for a multitude of industrial applications, it is heavily configurable and has lots of operating modes. 

<img src="https://practicalseries.com/2001-pal/31-git/01-pages/00-00-index/02-images/warning.svg?bxno=d0014A-001-000">

To avoid any confusion *(and, if I’m being honest, to avoid any liability)* I’m making this software available under the MIT Open Source licence. The MIT licence is a *“permissive”* licence; it is what most people think of when they think about open-source software. The licence is easy to comply with; essentially, you or your organisation need only reproduce the MIT licence and copyright notice, when using the code. Otherwise, you may do as you wish with the code, including modifying it, adding it to your software or just selling it. You must however, include the copyright notice.

<br />

Michael Gledhill <br> Chester &mdash; February 2021
