.. _hub-xctest:

Running test cases on XCTest
============================

**A.** Create a project in RobusTest which you shall be using for running your tests. This needs to be done only once. Note down the project ID. Project ID is the alphanumeric number in the URL of the project dashboard.

**B.** Upload the app enterprise build to your project and note down the build ID. This needs to be done everytime you have a new app build. Build ID is the name of the file that you get when you copy the URL to the build.

**C.** Upload zipped up App XCUITests file to your project and note down the build ID. This needs to be done everytime along with a new App enterprise build. Build ID is the name of the file that you get when you copy the URL to the build.

**D.** Get your ACCESS KEY from your profile page in RobusTest.

**E.** Once you have the three pieces of information above, invoke the test using the following API

* *API URL:* **<RobusTest URL>/v3/xcuitest/job/new?accesskey=<ACCESS KEY>**

* *API REQUEST TYPE:* **POST**

* *POST REQUEST BODY:*

|   **{**  
|     **"identifier":"<PR_NAME_GIVEN_BY_ENTERPRISE>",**
|     **"deviceVersion":"<iOS version of the device>",**
|     **"project":"<Project ID>",**
|     **"build":"<Build ID>",**
|     **"testBuild":"<Test Build ID>"**
|   **}**
