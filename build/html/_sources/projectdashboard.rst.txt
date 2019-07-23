Project Dashboard
=================

.. role:: bolditalic
   :class: bolditalic

.. role:: underline
    :class: underline

The Project Dashboard provides you information about the project you have created - i.e., the app under test, the build details, project members, CI settings, etc.

.. image:: _static/projectdashboard2.png
 	:align: center

Let's have a look at the Dashboard in detail.

The Project Dashboard constitiyes of the following 4 sections:

1. Builds
2. Team
3. Upload Build - Remote
4. Settings

**1. Builds**

This is the section of the Dashboard on which you land by default on clicking on a project.

The Build section provides you information about:

* *Build details* (i.e., build name, version name, version code, package name and launch action)
* *Description about the build*
* *Build file size*
* *Name of the team member who uploaded the build to the project*
* *Date of upload of the build to the project*

You can upload multiple builds to a project. You can choose the build to be tested upon from the 'Build' drop down field.

In addition to providing you the details about the build, this section of the Dashboard also allows you to perform the following tasks:

* *Upload New Build* - Clicking on this button enables you to manually upload an app build from a chosen location to the project
* *Get selected Build URL* - Clicking on this button copies to the clipboard, the URL to download the currently selected build in the project. On pasting this URL on a browsr tab and hitting enter, the user is able to download the currently selected build onto their computer.
* *Delete Selected Build* - Clicking on this button deletes the currently selected build from the project. Only a project member with admin privileges can delete a build.

**2. Team**

All members who are added to the project are listed on the Team setion. Apps that are part of a particular project can be accessed by everyone who is part of that project.

Project members have the ability to test, automate and view reports for any build that is part of their project.

Each team has 2 kinds of memebers - Admin and non-admin

Admin members have a few additonal privileges when compared to non-admin members. They can:-

* Delete a build from the project
* Add/remove members from the project
* Grant to/Revoke from a team member admin privileges
* Execute a CURL command to upload an app build remotely

By default, a member who creates a project has admin privileges on that project.

Note: *An Admin member of a project is different from a RobusTest Admin* The former's privileges are restricted to the project the member is a part of while the latter has special prvileges on the entire RobusTest platform

**3. Upload Build - Remote**

This section is visible only to admin members of the project.

Here, a CURL command is provided which enables the user to upload an app build to the current project remotely

The general format of this command is as follows:

#:bolditalic:`curl -X PUT '<PROJECT IDENTIFIER>h' -H 'content-Type: multipart/form-data' -F build=@<BUILD NAME WITH PATH>`

**curl -X PUT '<PROJECT IDENTIFIER>h' -H 'content-Type: multipart/form-data' -F build=@<BUILD NAME WITH PATH>**


Here the app build present in the location  or path mentioned in the command is uploaded to the project that is identified by the Project Idenitifier.

The 'Project Identifier' is provided in the section while the path to the location from where the build may be picked up can be specified by a team member.

You can now run the above command directly on the command line OR choose to invoke the above build-upload API through a programming script in a language of your choice.

E.g. you can add the above line to your Jenkins shell script that creates a new build. As a result, whenever a new bui;d gets created, it also gets uploaded to the project. Using RobusTest, you can now build a process, say, to test this new build by running a sanity or smoke test each time a new build that is uploaded to the project.


**4. Settings**

This section provides you the following options:

*a. Enable notifications* - On enabling this checkbox, each member of the team is notified whenever a new build is uploaded to the project

*b. Choose Bug Tracker configuration* - RobusTest supports Continuous Integration with your existing CI tools through APIs. 

Once you have integrated your Bug Tracker tool wih RobusTest, this configuration will be available for selection in the 'Bug Tracker' drop down. Once the required configuration is selected, all bugs encountered during your testing can be logged directly, from RobusTest, into the tool of your choice.

You can configure your project with the tool of your choice through the 'Integration' section of the RobueTest Admin Console.