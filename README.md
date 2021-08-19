<table>
<tr>
<td>
<img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/gsoc_logo.png" align="top">
</td>
<td>
<img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/librehealth.png" align="top">
</td>
</tr>
</table>

## Organization - LibreHealth

## Project - Scaling up the mobileHBS/DHIS2 Tracker and Trainer applications

## Student - Bhavesh Sharma

### Goal 

In various low/middle-income countries children die in just a few days after their birth due to the inadequate supply of facilities that they require. The important fact is that all of these deaths are Preventable and can be prevented by providing proper knowledge to the mothers of the babies and other people and by providing a proper tracker facility to track the health status of the baby in the early days of his birth.

As a sort of solution MHBS applications are launched which is a set  of 4 applications. Out of which I had worked on the mhbs-trainer and mhbs-tracker. Tracker is used for data collection which is built from the dhis2 mobile application and trainer is used to access the resources.

The Goal of this project is to develop the scale-up version of the existing mHBS application, updating the old code base and adding new features, providing a feature to access media resources uploaded on the dhis2 through the trainer app which will be used for the training of the individual.

### Links

#### Librehealth Project Repository 

  - mHBS-Tracker Project   https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker

  - mHBS-Trainer Project   https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer

#### My Forked Repository 

  - mHBS-Tracker Project  https://gitlab.com/bhavesh3005sharma/mHBS-tracker

  - mHBS-Trainer Project  https://gitlab.com/bhavesh3005sharma/mHBS-trainer

#### Mobile App
                         
  - Link to mobile app : [`Tracker-APK-Link`]()  [`Trainer-APK-Link`]()
                         
### What was done:

During these 10 Weeks, I have:

  - Updated mHBS-Tracker repository with latest dhis2 one & made changes required for tracker app.
  - Added Media Page, Integrated API Calls to fetch and play all type of media files (educational resources) uploaded in dhis2.
  - Added offline support & sync facility.
  - Build a system to track app usage.


## Merge Requests

1. #### Update mHBS-Tracker & Set-up CI/CD - [Merge Request 12](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/merge_requests/12) - status:-**Merged**

  - Merged the upstream changes that have more than 6K unmerged commits.
  - Modified the final merged code to have features and look like the mHBS app.
      * App Name and Logo has been changed.
      * UI Improvements.
      * Added External other apps of mHBS to the app drawer.
      * Added functionality to open other mHBS apps.
  - Set up CI/CD to automatically build the app and check for errors.
  - Fixed Some of the build errors.

2. #### Added Media Page | Added Feature to play any type of media file | Set-up CI Pipeline - [Merge Request 194](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/merge_requests/194) - status:-**Merged**

  - Added Media Page in trainer app and uploaded some educational & testing resources on dhis2.
  - Integrated API Calls to fetch media resources into trainer app.
  - Integrated cordova-file-opener2 plugin and make all types of media files accessible through the app.
  - Integrated Gitlab CI Pipeline to automatically build the apk.
  - Related Issues : [#190](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/190)    [#112](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/112)   [#77](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/77)   [#39](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/39)   [#21](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/21)

3. #### Added offline support - [Merge Request 195](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/merge_requests/195) & [Merge Request 198](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/merge_requests/198) -  status:-**Merged**

  - Implemented File sync feature and added appropriate synced icon for stages.
  - Implemented sqlite-database and cordova file plugin to storage purpose.
  - Added full offline support for synced media files.
  - Sync facility is added for both the list of documents and for document media files as well.
  - Related Issues : [#69](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/69) 

4. #### Added System to track app usage - [Merge Request 196](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/merge_requests/196) -  status:-**Merged**

  - App usages are being stored locally in the SQL database ( like Page visits, Time spent, etc.).
  - After crossing the min. threshold limit app usage will get synced with the dhis2 user’s datastore and shifted to dhis2.
  - Overall usage of each page (approx 15+ pages) can be tracked remotely over dhis2 and can be used for analytical purposes.
  - Related Issues : [#36](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/36) [#120](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/120)

5. #### UI Improvements & Filtering Options - [Merge Request 199](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/merge_requests/199) -  status:-**Merged**

  - Added Thumbnail and video duration in media files.
  - Added filtering options for media files to sort them in categories by their types.
  - Improve UI, added button. 
  - Related Issues : [#195](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/195)
    
6. #### Exported Mhbs Tracker app Metadata - [Merge Request 16](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/merge_requests/16) -  status:-**Merged**

  - Exported tracker specific metadata from dhis2.
  - Checked the metadata by importing it on Demo Dhis2 Servers as well.
  - Related Issues : [#22](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/22)

 
7. #### Passed user credentials to trainer app - [Merge Request 13](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/merge_requests/13) -  status:-**Merged**

  - Shared login credentials of tracker app with the trainer app.
  - There is a single login in the tracker app and all the other connected apps will use that credentials for further process, users needs not to logged in again and again in all mhbs apps.
  - Related Issues : [#16](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/issues/16).
   
## Other Supporting MRs & Tested/Fixed Issues

  - [MR-201](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/merge_requests/201) | [Issue-196](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/196) - Updated cordova secure storage plugin.
  - [Issue-14](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/issues/14) - View data completion form.
  - [Issue-13](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/issues/13) - Create `seconds` data element for OSCE B.
  - [Issue-10](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/issues/10) - Tested all the features of [Module_1_mHBS_General_User_Guide_JANUARY_30_2019_FINAL.pdf](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/uploads/0728128fc5240cbd2797e0d707dd27ae/Module_1_mHBS_General_User_Guide_JANUARY_30_2019_FINAL.pdf) in the new tracker app.
  - [Issue-11](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/issues/11) - Need to change frequency of tracker forms and HBB survey.
  - [Issue-12](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/issues/12) - Need to modify HBB infrastructure survey.
  - [MR-14](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/merge_requests/14) | [Issue-4](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/issues/4) - Fixed mHBS logo.
  - [MR-15](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-tracker/-/merge_requests/15) - Fixed mHBS tracker app CI-Pipeline.
  - [MR-197](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/merge_requests/197) | [Issue-193](https://gitlab.com/librehealth/incubating-projects/mhbs/mHBS-trainer/-/issues/193) - Removed embedded - Keeping baby warm video.

## What after GSoC

I will continue to contribute to LibreHealth for this project. I will assist the new members who are willing to contribute for this project. I will actively take part in the discussions and I will contribute by creating, Solving issues and adding improvements to this app. Currently the on-campus Intern hirring process is also going on, focus on that as well.

## Thanks to my mentors

I would like to thank my mentors, **Sherri Bucher, Saptarshi Purkayastha, Robby O Connor** for being so nice and helpful. I have learnt a lot in the past 2-3 months and it has been a great experience to be a part of this wonderful organisation.

I am very much thankful to **Saptarshi Purkayastha**, I am very grateful to you, this was all possible because of your encouragement, advice, and support that you’ve given me. You have been incredibly generous with your time and energy, Your words of encouragement brightened me & helped sharpen my skills.

## Screenshots

### mHBS-Trainer App
|  |  | |
| ------ | ------ | ------ |
| <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/trainer-home-page.png" align="top">| <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/trainer-media-page-allmedia.png" align="top"> |  <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/trainer-media-page-pdfs.png" align="top"> |
| Home screen | Media Page showing all media files tab | Media Page showing PDF media files tab |
|   <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/trainer-media-page-videos.png" align="top">| <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/trainer-media-page-others.png" align="top"> |
| Media Page showing video media files tab with thumbnail & video duration | Media Page showing other media files tab    

### mHBS-Tracker App
|  |  | |
| ------ | ------ | ------ |
| <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/tracker-splash-screen.png" align="top">| <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/tracker-splash2.png" align="top"> |  <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/tracker-home-page.png" align="top"> |
| Splash Screen |  Configuration Syncing Page |   Home screen showing all Programs and Data Sets |
|   <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/tracker-home-nav-drawer.png" align="top">| <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/tracker-enrollment.png" align="top"> | <img src="https://github.com/bhavesh3005sharma/GSoC-assets/blob/master/gist_images/tracker-OSCE-B.png" align="top"> |
|   Home screen showing navigation drawer |   Tracker Enrollments Page | OSCE-B Form

## Communication

The project [chat channel](https://forums.librehealth.io/t/project-scaling-up-the-mobilehbs-dhis2-tracker-and-trainer-applications/4156) is on Librehealth Forums, my entire communication with my mentors can be seen there.

## Blog posts during GSoC

For better understanding of implementation details & other works done by me please check my [Weekly Bogs](https://bhavesh3005sharma-gsoc21.blogspot.com/).
