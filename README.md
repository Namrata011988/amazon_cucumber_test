# amazon_cucumber_test
Test automation for amazon search using cucumber bdd

**Task Details - **

Below is the requirement - 
Create Selenium Web browser tests using Java language for amazon.com with following details:
- Search Nikon and sort results from highest price to lowest.
- Select second product and click it for details.
- From details check (verify with assert) that product topic contains text “Nikon D3X”

 Additional points for -
 - Creating Cucumber scenario which is used for test execution/test step mapping.
- Implementing the webpage opening step so that url is parameter
- The test is implemented as Maven project and the test can be executed from command line using command: mvn clean test. Inspector will set suitable path to the Chrome/Firefox drivers.

**Solution details -**
- Created a maven project, containing selenium test for amazon search and validation, using cucumber bdd libraries.
- Project contains below details
  - pom.xml, which contains the required junit, selenium and cucumber libraries.
  - feature file (**amazonSearch.Feature**), which contains the scenario and the steps which are then mapped to the test steps.
  - step definition file (**amazonSearchSteps.java**), where the test steps and assertion is implemented.
  - runner file (**TestRunner.java**), used for test execution.
  - Web page opening step is parameterized by using scenario outline and examples within the feature file.
  - Just to mention, another way to parameterize the url, is to pass it through the (junit or mvn )configuration. (not implemented within the solution).
  - Test is implemented within a maven project and can be executed using mvn clean test command.(mvn clean test -Dbrowser=firefox)
  - Test is created to accept the browser from the user, in case browser is not mentioned default browser is set as firefox
  - Driver path needs to be mentioned in the run configuration parameters as per the screen shot -
  -![image](https://user-images.githubusercontent.com/52945610/109395013-c7106c00-7932-11eb-9221-cb51d8bdb2f0.png)
  
  - **Test is implemented for both firefox and chrome, but it doesnt work well with chrome as it takes me to the captcha page, which i have not handled with the code. This is something new for me to learn, as till now i have been using a mode in which the dev team has disabled the google captcha.
**
