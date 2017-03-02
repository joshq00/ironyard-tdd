### Example

![][GMT]

[GMT]: images/gmt/app.png

note:
- This is from a legacy app
- One of the first things I worked on when I joined team
- About 300k lines of code
- 289 API endpoints


![][GMT-1]

[GMT-1]: images/gmt/switch.png "Route switch"

note:
- Teams using BLUE/GREEN
  - two versions of their app
  - deploy, make sure it works
  - then switch traffic


![][GMT-2]

[GMT-2]: images/gmt/switching-custom.png "Custom route switch"

note:
- have to open a ticket
  - person working ticket comes here
    - click switch
    - also click the correct radio option
- correct radio:
  - if bottom right, go top left, vice-versa


![][GMT-3]

[GMT-3]: images/gmt/switching-single.png "Single route switch"

note:
- if it's one of the left options,
  - dont click switch
  - pick the correct radio


<video controls class="speed-4x"><source src="images/gmt/finding service.mov"></video>

note:
- logic was very complex and intertwined with
  lots of other screens
- took a long time to get tests to run
- 15 total tests
  - only 11 passed
- none of the tests were for this screen


#### === no confidence
note:
- wasn't comfortable changing the code
- ended up building a separate service that
  called the API with the correct values
- with 100% test coverage
  - anyone can change that and know if they broke it

