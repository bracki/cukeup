!SLIDE incremental
# The Münchhausen Move #
## (where the bootstrapping happens) ##
!SLIDE
# Spec the application driver layer by writing Cucumber scenarios

!SLIDE
# Where it gets all meta!

!SLIDE

    @@@ cucumber
    Feature: Manage websites via REST API
      As a jimdo developer
      I want to manage websites via a REST API
      So that I can test new features easily

!SLIDE smaller

    @@@ cucumber
    Scenario: Create a new website
      When I send a POST request to "/api/websites" with body
      """
      {
        "username" : "cucumber",
        "title" : "Can I haz Cukes?"
      }
      """
      Then the response is application/json
      And the status is 200 OK
      And I can reach the website with username "cucumber"
      And the website html title is "Can I haz Cukes?"

!SLIDE
## Use the API to replace the Given steps' implementations in the Scenarios.

!SLIDE smaller
# Before
    @@@ cucumber
    @browser @rest-api
    Feature: REST API and browser testing works

    Background:
      Given I send a POST request to "/api/websites" with body
        """
        {
          "username" : "cucumber",
          "title" : "Hello world.",
          "pages" : [
            { "title": "Cucumber rocks!" }
          ]
        }
        """
     And the response is JSON and the status is 200 OK
     And I can reach the website with username "cucumber"

    Scenario: Hello World!
      When I navigate to the website "cucumber"
      And I log in with "jimdo"
      Then I see the page "Cucumber rocks!" in the navigation

!SLIDE smaller 
# After
    @@@ cucumber
    @browser @rest-api
    Feature: REST API and browser testing works

    Background:
      Given I have a website named "cucumber"
      And a page named "Cucumber rocks!"

    Scenario: Cucumber rocks. 
      When I navigate to the website
      Then I see the page "Cucumber rocks!" in the navigation

!SLIDE

# Simple teardown 

    @@@ ruby
    After("@rest-api") do
     # always cleanup the test websites
     http_req("DELETE", "/api/websites")
    end


!SLIDE
# Outside in at its best. 
