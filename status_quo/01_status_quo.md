!SLIDE bullets 
# Status Quo Ante BDD #

* How we previously handled our stuff

!SLIDE bullets
## Acceptance criteria tracked in various Excel Sheets

* Manually executed by the whole team
* Ending up in "test fests", possibly going on for a couple of days
* If taken seriously, that means locking up the whole team for every new feature
* Varying levels of detail

!SLIDE bullets incremental
## Some of those have been converted to Selenium by a consultant

* Soon got excluded from testsuite
* Because lost knowledge...
* Lead to unmaintained tests

!SLIDE
## Unclear requirements esp. due to i18n

* Coordinate your features with all stakeholders
>One step forward, two step backwards, down in a Babylon

!SLIDE bullets
## The good parts

* Automatic Deployment with ~hourly updates
* Test environment is an exact replica of the live system

!SLIDE
# Biggest drawback

# No bloody fixtures!?

* Meaning no setup!
* Meaning no teardown!
* Meaning, resetting your tests manually by SSHing into various systems and deleting entries from MYSQL, oh no!!!!

!SLIDE bullets incremental
# Violation of the FIRST principle

* Fast
* Independent
* Repeatable
* Self Validating
* Timely

!SLIDE
# Tests are ...

* neither independent
* nor repeatable
* thus basically maiming all Given, Before and After steps
