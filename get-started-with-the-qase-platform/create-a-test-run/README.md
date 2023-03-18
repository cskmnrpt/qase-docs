# Test cases

### What is a test case in software testing?

A test case contains all the details about our test. A title is enough to create a quick test case. For a more detailed test case, you can define prerequisites, steps, expected and actual results, etc.

{% embed url="https://youtu.be/m7CaA5J30NI" %}

### Create Test Case

#### **Quick test case**

1. On the page, under your test suite click on the link “+ Create quick test”
2. The cursor will start blinking on the page, and you can start typing the title. Click Enter to save the test case. As a result, a new test case under the test suite is shown with ID and a title.

This is the fastest way to add a test case, let’s see how to create a more sophisticated one.

#### Detailed test case

1. On the main repository page, click on the button “+ Case”. As a result, a new page “Create test case” is shown. Test case properties are divided into several sections:
   * _Title:_ define the name of a test case
   * _Status:_ can be either Active, Draft, or Deprecated
   * _Description:_ additional details for more context about a test case
   * _Suite:_ choose here which Test Suite your new case belongs to
   * _Severity:_ can be either Trivial, Minor, Normal, Major, Critical, Blocker, or Not Set
   * _Priority:_ can be either Low, Medium, High, or Not Set
   * _Type:_ select what type of testing is applicable for your test case
   * _Layer:_ pick a layer of the test case, whether it's an end-to-end, API, or a unit test
   * _Is flaky:_ if a test case is unstable, you can mark it as flaky
   * _Milestone:_ select whether a test case is related to one of your Milestones, which you can create separately
   * _Behavior:_ can be either Destructive, Negative, Positive, or Not Set
   * _Automation Status:_ you can choose from Automated, To Be Automated, or Not Automated
2. To save a test case click on the button “Save”. As a result, the page “Test repository” is shown with a new test case. Icons with arrows in front show the priority and severity of the test case.
