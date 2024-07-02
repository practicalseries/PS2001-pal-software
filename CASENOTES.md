<hr />

# PAL &mdash; Case Notes <img height="25px" src="https://img.shields.io/badge/CASENOTES.md-2024--05--08-4F81BD.svg">

These case notes are intended as a brief points list of current and upcoming items within the _PAL software development_. In short: notes to myself, a sort of _aide-memoire_ of things I need to do (or at least think about).

It is written in the form of an engineering log book in reverse chronological order (most recent at the top). I know that GitHub provides similar facilities: issues, milestones, actions &c. all of which have their uses. I just wanted something that was a bit more free-flowing and less official. I also wanted something that I could keep in the main repository (on my PC) rather than something that I could only access via GitHub.

This Case Notes file was created on May 8th, 2024.

Michael Gledhill
Chester &mdash; May 2024

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
- [ ] SMDS for UT00851 change USER_DESC to USER_INFO
- [ ] SMDS for UT00852 change USER_DESC to USER_INFO
- [ ] SMDS for FC02001 change USER_DESC to USER_INFO
- [ ] SMDS for FC18001 change USER_DESC to USER_INFO
- [ ] Update FC18001 (AI read subroutine) with DB00801/851 interface
- [ ] Update FC18001 (AI read subroutine)with comments from revised SMDS
- [ ] Update FC02001 (Inst read and scale) with DB00801/851 interface
- [ ] Update FC02001 (Inst read and scale) with comments from revised SMDS
- [ ] Retest/reissue FC18001
- [ ] Retest/reissue FC02001
- [ ] Write FC18002 AQ Scale



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
