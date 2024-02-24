# Certified Pega System Architect
* https://academy.pega.com/exam/certified-pega-system-architect-4
* https://academy.pega.com/mission/system-architect/v5

# Exam topics

* Case Management (33%)
  * Design a [case lifecycle](https://academy.pega.com/module/defining-customer-microjourney/v5/in/36626/37366), [stages](https://academy.pega.com/topic/case-life-cycle/v4/in/36626/37366/37466), [set case statuses](https://academy.pega.com/topic/case-status/v3/in/36626/37366/37501), add instructions to tasks
  * [Add a service level agreement; configure urgency, goals, deadlines, passed deadlines](https://academy.pega.com/module/completing-work-time/v5/in/36626/37366)
  * [Route assignments to users and work queues](https://academy.pega.com/module/routing-assignments-users/v5/in/36626/37366)
    * Note: work group is more "high level" then work queue
  * Configure [approval processes](https://academy.pega.com/module/designing-approval-process/v5/in/36626/37366): cascading approvals, reporting structure, authority matrix
  * [Configure and send email correspondence](https://academy.pega.com/module/sending-emails-during-case-processing/v5/in/36626)
  * [Identify duplicate cases](https://academy.pega.com/module/identifying-duplicate-cases/v4/in/36626/36956)
    * For cases that meet the basic conditions, the system continues to evaluate the weighted conditions for duplicate cases. When the total weighted value for a case meets or exceeds the threshold value, the case is flagged as a potential duplicate
  * [Identify and add optional actions](https://academy.pega.com/module/adding-optional-actions-workflow/v6/in/36626/36956)
    *  A series of steps that are not the usual path can be handled with an optional process.
  * [Automate workflow decisions using conditions](https://academy.pega.com/module/automating-workflow-decisions/v4/in/36626/36956)
  * Pause and resume case processing; wait steps
  * Skip a stage or process
  * [Configure child cases](https://academy.pega.com/module/creating-child-case/v5/in/36626/36956)
  * [Understand when to use automation shapes](https://academy.pega.com/module/automation-shapes-case-life-cycle/v3/in/36626/36956)
  * Automate decisions using decision tables and decision trees
  * Create and manage teams of users
* Data and Integration (23%)
  * Configure data types, create data objects, [data relationships, and field types](https://academy.pega.com/topic/data-relationships/v3/in/36626/37366/37596)
  * [Identify and create calculated values](https://academy.pega.com/topic/calculated-values/v4/in/36626/37366/37571)
  * [Validate data](https://academy.pega.com/module/validating-data-dev-studio/v5/in/36626/44381); create and configure data validation rules by using business logic
    * Complex validation scenarios, like validating the length of a data element and so on, must be configured in Dev Studio.
    * Functions present a customized set of fields for configuring validation behavior
 
  * [Manipulate application data, set default property values, configure data transforms](https://academy.pega.com/module/application-data-manipulation/v5/in/36626/44381)
    * Best practice is to use the *Data initialization* page when setting a default for a field to a static value
  * Access sourced data in a case; refresh strategies; populate user interface controls
  * Save data to a [system of record](https://academy.pega.com/topic/data-objects/v2/in/36626/37366/37596)
  * Simulate and add external data sources
  * Capture and present data: fields and views
  * [View data in memory: clipboard tool, pyWorkPage](https://academy.pega.com/module/viewing-data-memory/v5/in/36626/44381)
    * Clipboard page organization
      * User Pages
      * Data Pages
      * Linked Property Pages (read only pages)
      * System Pages
  * Configure field values
  * Create and set application settings
* Security (5%)
  * Manage user and role assignments
  * Configure security policies
* DevOps (5%)
  * Record a unit test
  * Create and execute scenario-based test cases
  * Identify best practices for configuring unit tests
* User Experience (12%)
  * Customize user interface elements: dashboards, portal content
  * Configure action sets
  * Customize form appearance, visibility settings, controls
  * Add and remove fields
  * Group fields in views
  * Display list data in views; configure repeating dynamic layouts
  * Localize application content
  * Enable accessibility features in an application
* Application Development (12%)
  * Manage application development: user stories, feedback, bugs
  * Use the Estimator tool to scope a Pega Platform project
  * Create and maintain rules, rulesets, classes, inheritance
  * Debug application errors
* Reporting (5%)
  * Create business reports
  * Identify types of reports
Use columns and filters
Describe the benefits of using Insights
* Mobility (5%)
Configure mobile app channels
Use of Pega Mobile Preview
