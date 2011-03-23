!SLIDE bullets 
# Status Quo Ante Cucumerem #
* How we previously handled our stuff

!SLIDE bullets incremental
# Acceptance criteria tracked in various Excel Sheets

* Varying levels of detail,
* often documenting the implementation instead of expecting behaviour

!SLIDE bullets incremental

* Manually executed by the whole team
* Ending up in "test fests", possibly going on for a couple of days
* If taken seriously, that means locking up the whole team for every new feature

!SLIDE bullets incremental
# Some of those have been converted to Selenium by a consultant

* Soon got excluded from testsuite
* Because lost knowledge...
* Lead to unmaintained tests

!SLIDE bullets incremental
# Unclear requirements esp. due to I18N

* What are the VAT regulations in Japan?
* How do I refund a double booking from Kazakhstan?
* What's the format for postal addresses in Poland? 

!SLIDE
# It's not a bug report!

!SLIDE
# It's a feature _request_!

!SLIDE
# _One step forward, two step backwards, down in a Babylon..._

!SLIDE bullets incremental
# The good parts

* Automatic Deployment with ~hourly updates
* Test environment is an exact replica of the live system
* Excellent support team
* Log aggregation

!SLIDE
# The biggest drawback

!SLIDE
# No bloody fixtures!

!SLIDE bullets incremental
# No bloody fixtures!?

* Meaning no setup!
* Meaning no teardown!
* Meaning, resetting your tests manually by SSHing into various systems and deleting entries from MySQL, oh no!!!!

!SLIDE bullets incremental
# Violation of the FIRST principle

* Fast
* Independent
* Repeatable
* Self Validating
* Timely

!SLIDE bullets incremental
# Tests are ...

* neither independent
* nor repeatable
* thus basically maiming all Given, Before and After steps
