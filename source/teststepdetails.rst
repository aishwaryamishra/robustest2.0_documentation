.. _test-step-details:

Test Step Details
=================


6. Test Step Details 
   a. Basic 
   b. Settings
   c. User Data
   d. Return Data 
   e. XPath 
   f. Script 
   g. References 
   h. Dependencies
   i. Function Steps


For any recorded test step, if you click on the 'Show Step Details' button, you can see that the test step expands to reveal the following tabs:

**a. Basic** 
**b. Settings**
**c. User Data**
**d. Return Data** 
**e. XPath** 
**f. Script** 
**g. References** 
**h. Dependencies**
**i. Function Steps**

These tabs provide you more information about and control over the automation test steps you have created. Let's have a look at each of these tabs in detail.

**a. Basic** 

This tab let's you provide a name and a description for the test step that has been recorded.

Whenever you record a test step, by default, RobusTest provides you a test step name depending on the element and the action that was performed. Sometimes, this default test step may not be easy to understand. E.g. a step named 'Tap on Relative Layout'.

In such cases, the user can go to the Test Step Name field under the 'Basic' tab and rename the step to something more meaningful. E.g. 'Tap on Play button icon'

**b. Settings**

For test steps that record a user action such as a tap, type, swipe, etc, the 'Settings' tab provides certain configurable paramters.

* *onFail* - This prameter determines what action should be performed at the end of execution of a test step. This field can have the following values:
   * *Fail* - This is the default value. If the test step is not executed successfully, the succeeding test steps *are not* executed and the test case is considered to have failed.
   * *Continue* - In this case, even if the test step is not executed successfully, the succeeding test steps *are* still executed.  and the test case is considered to have failed.
   


**c. User Data**
**d. Return Data** 
**e. XPath** 
**f. Script** 
**g. References** 
**h. Dependencies**
**i. Function Steps**



Older text:

- - - - - - - - - -

Every action that you record on the app is added as a step in the test case table.
There are many useful option available as part of the Recording session.

1. If you wish to delete a step you can do that by clicking on the delete button.
2. If you wish to re-run a step or a group of steps, you can do that by selecting the steps and clicking on the Run Steps button in the header.
3. You can save your test case and continue the recording session. Once you have saved your test case, you could either update it or create a new one.
4. You can also edit the name of the test step to make it more intuitive.
5. An orange highlighter points to the location of the current execution pointer
6. The pin icon in the Action column enables user to select the current execution point

When a user clicks on a text field, the system shows a text box to enter the text value.
When user enters a value in the text box, this is recorded as an input value for the field.

After a test case has been created, click on the Save button to provide a name and save this test case. Click on End session to close the recording session without saving the test case.

Upon saving the test case, you will see your saved test case along with the actual test script and related information. There are four tabs on the test case page.

1. Test Step: This tab lists the steps of the test case
2. Test Script: This tab shows the test script to be executed when the automated test case runs. The script is shown in a smart script editor. If the user wishes to add custom code to his/her test scripts, s/he can do that in this script editor. The editor also checks for syntax correctness.
3. Meta Data: The test script has been designed in a modular way to separate the app objects from the test script. This ensures that the test case can be easily updated and maintained as builds change over time.
4. User Data: In line with the modular design, the user data too is separated out from the test script and is available in the User Data tab.

- - - - - - - - - - 