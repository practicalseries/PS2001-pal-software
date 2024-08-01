<hr />

# PAL &mdash; Case Notes <img height="25px" src="https://img.shields.io/badge/CASENOTES.md-2024--05--08-4F81BD.svg">

These case notes are intended as a brief points list of current and upcoming items within the _PAL software development_. In short: notes to myself, a sort of _aide-memoire_ of things I need to do (or at least think about).

It is written in the form of an engineering log book in reverse chronological order (most recent at the top). I know that GitHub provides similar facilities: issues, milestones, actions &c. all of which have their uses. I just wanted something that was a bit more free-flowing and less official. I also wanted something that I could keep in the main repository (on my PC) rather than something that I could only access via GitHub.


This Case Notes file was created on May 8th, 2024.

Michael Gledhill
Chester &mdash; May 2024

<hr />
<br />

## 0005 &mdash; ENGINEER'S LOG &emsp;&emsp; &emsp;&emsp; <img height="25px" src="https://img.shields.io/badge/Date-2024--07--13-00B050.svg">

| Branch             | Associated Commits
| ------------------ | -----------------------------------------------------
| **master** | <img  eight="20px" src="https://img.shields.io/badge/Dev-D0017-000000.svg">
| **D0017A-FC18002** | <img src="https://img.shields.io/badge/Dev-D0017A--000--106-BF504D.svg"> 

<br />

### Thoughts

_I'm beginning to think it may be better to rely on PDFs for block comments rather than transcribing the full extent of the SMDS into the block comment fields. The conversion process is taking a long time (longer than it takes to write the block in the first place) and it is difficult to keep the comments up to date with any SMDS changes._

_It's a bit of a bastard. I've noticed it now because I'm re-working the anaglog read blocks to incorporate the UT/DB00801/802/851/852 constants and I'm effectively having to modify the same document twice (firstly the SMDS in Word and secondly the comment fields in the module in TIA Portal) and this seems daft. Better I think to modify the SMDS, convert it to a PDF and put it in the User Doc area of the TIA Portal project._ 

_The comment fields are a right pain in the arse, especially the tables, it takes ages to get everything lined up (I've also noticed that any scaling introduced on 4K/5K monitors screws the spacing up); again, the UserDoc route seems to be the way to go. That said, I do like having all the information available in the comment fields, it appeals to my engineering conservatism &mdash; it means the block information is always there and can't be stripped out of the project. Hmmm._

_So my idea is this:_

1. Limit the block comments to the title, abstract and technical information _(possibly the functional description, parameters? where do you stop?)_
2. Begin incorporating the PDF version of the SMDS into the UserDoc area of the project
3. Change the SMDS PDF documents available via the website to use the same filename as the UserDoc PDFs (for consistency)

_It leads to some problems though:_

1. How are User Docs handled within the Siemens Version Control Interface and VSCode/GitHub?
2. It's a lot of PDF data to put on GitHub (shouldn't have PDFs in the repository)
3. How do I track the PDF versions and ensure that they're up to date?


### Outstanding items
- [x] FC02001 &mdash; change out of range calculation to be based on scaled range rather than raw range (SMDS updated too) <img height="20px" src="https://img.shields.io/badge/-D0017A--000--106-BF504D.svg">
- [ ] FC18001 &mdash; change out of range calculation to be based on scaled range rather than raw range
- [X] Add OVER/UNDER range limits to UT00851
- [ ] Add OVER/UNDER range limits to UT00852
- [X] Add OVER/UNDER range limits to SMDS DB00851
- [ ] Add OVER/UNDER range limits to SMDS DB00852
- [ ] Modify SMDS FC02001 for OVER/UNDER range limits 
- [ ] Modify SMDS FC18001 for OVER/UNDER range limits 

>*Note:&emsp;Orignally, the out of range was calculated as a function of the RAW range (RAW_MAX-RAW_MIN), the problem with this is that the our of range limits would be different for bipolar/unipolar ranges. Better to calculate the out of range value from the scaled range, this will return the same results irrespective of the raw input type.*
>* My other thought on this is that if the OOR is set too high, it may be beyond the range of the actual RAW input (i.e. outside the numerical range of the analog input itself), I'm not sure how to check this, it depends on the uni/bipolar range of the card itself.*

<hr />
<br />


## 0004 &mdash; ENGINEER'S LOG &emsp;&emsp; &emsp;&emsp; <img height="25px" src="https://img.shields.io/badge/Date-2024--07--02-00B050.svg">

### PAL Website Development

<br />

- [ ] Update standard web engine for PAL website (review all CSS/HTML exisiting files and pages)
- [ ] Update Google analytics
- [ ] Add Google programmable search engine to site (all pages in nav bar)
- [ ] Put together landing pages for base website, add links to project documentation and install sitemap and analytic file for Google.

<hr />
<br />


## 0003 &mdash; ENGINEER'S LOG &emsp;&emsp; &emsp;&emsp; <img height="25px" src="https://img.shields.io/badge/Date-2024--06--13-00B050.svg">

| Branch             | Associated Commits
| ------------------ | -----------------------------------------------------
| **master** | <img  eight="20px" src="https://img.shields.io/badge/Dev-D0017-000000.svg">
| **D0017A-FC18002** | <img src="https://img.shields.io/badge/Dev-D0017A--000--106-BF504D.svg"> 

<br />

### Outstanding items
- [x] UT00851 change USER_DESC to USER_INFO <img height="20px" src="https://img.shields.io/badge/-D0017A--000--106-BF504D.svg">
- [x] UT00852 change USER_DESC to USER_INFO <img height="20px" src="https://img.shields.io/badge/-D0017A--000--106-BF504D.svg">
- [x] SMDS for UT00851 change USER_DESC to USER_INFO
- [x] SMDS for UT00852 change USER_DESC to USER_INFO
- [x] SMDS for FC02001 change USER_DESC to USER_INFO
- [ ] SMDS for FC18001 change USER_DESC to USER_INFO
- [ ] Update FC18001 (AI read subroutine) with DB00801/851 interface
- [ ] Update FC18001 (AI read subroutine) with comments from revised SMDS
- [x] Update FC02001 (Inst read and scale) with DB00801/851 interface
- [x] Update FC02001 (Inst read and scale) with comments from revised SMDS
- [ ] Retest/reissue FC18001
- [x] Retest/reissue FC02001
- [ ] Write FC18002 AQ Scale SMDS



<br />

### Outstanding items
- [ ] FC18002 (Analog output write) create and build

<hr />
<br />


## 0002 &mdash; ENGINEER'S LOG &emsp;&emsp; &emsp;&emsp; <img height="25px" src="https://img.shields.io/badge/Date-2024--06--02-00B050.svg">

1. Add enumerated "STATUS" variable (reflecting opened, closing, starting &c.) to all device types to allow GraphicIO objects to interact better
<hr />
<br />


## 0001 &mdash; ENGINEER'S LOG &emsp;&emsp; &emsp;&emsp; <img height="25px" src="https://img.shields.io/badge/Date-2024--05--11--CLOSED-808080.svg">

| Branch             | Associated Commits
| ------------------ | -----------------------------------------------------
| **master** | <img  eight="20px" src="https://img.shields.io/badge/Dev-D0017-000000.svg">
| **D0017A-FC18002** | <img src="https://img.shields.io/badge/Dev-D0017A--000--104-BF504D.svg"> 

<br />

### Outstanding items
- [x] UT/DB00800 to be renamed UT/DB00801 (inline with analog input and output subroutines)
- [x] Write/test runtime AI parameterisation using DB00801 and update SMDS with example code
- [x] UT/DB00851 (SCALE_VALUE) structure to be developed, common values to be added
- [x] Update FC02001 (analog instrument read/scale) with DB00801/DB20801 interface

<hr />
