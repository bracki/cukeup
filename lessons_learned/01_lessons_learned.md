!SLIDE bullets incremental
# Our stack

* [watir-webdriver](https://github.com/jarib/watir-webdriver)
* [Jenkins](http://jenkins-ci.org/)
* [Xvfb](http://www.x.org/archive/X11R6.8.1/doc/Xvfb.1.html)

!SLIDE
# watir-webdriver

    @@@ ruby
    @browser.goto('jimdo.com')
    @browser.div(:id, 'header')
            .ul(:class, 'nav').links

!SLIDE center
# Jenkins
![Jenkins - Test Trend](trend1.png)

!SLIDE
# Common Pitfalls

!SLIDE center 

    @@@ ruby
    timed out after 30 seconds
    (Watir::Wait::TimeoutError)

!SLIDE center smaller

    @@@ ruby
    Element is no longer attached to the DOM
    (Selenium::WebDriver::Error::ObsoleteElementError)

