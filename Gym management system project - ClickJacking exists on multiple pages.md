# Gym management system project - ClickJacking exists on multiple pages

[College Attendance System (CAS)](https://www.sourcecodester.com/visual-basic-net/15538/college-attendance-system-cas.html) Posted by SourceCodester is vulnerable to ClickJacking.

Attackers can use this vulnerability to deceive users to click, causing losses to individuals and platforms.



## The following pages are paths without the secure X-Frame-Options header:

```
/mygym/login.php

/mygym/signup.php

/mygym/admin/login.php

/mygym/admin/add_exercises.php

/mygym/admin/add_trainers.php

/mygym/admin/index.php
```



## The following takes /mygym/login.php as an example

![image-20220812164814061](Gym%20management%20system%20project%20-%20ClickJacking%20exists%20on%20multiple%20pages.assets/image-20220812164814061.png)



To detect whether there is a ClickJacking vulnerability, here we find that the response packet does not contain the X-Frame-Options: deny field, then we can construct an HTML file locally and use an iframe to include this page

![image-20220812165018782](Gym%20management%20system%20project%20-%20ClickJacking%20exists%20on%20multiple%20pages.assets/image-20220812165018782.png)



We can successfully load this page

![image-20220812165121053](Gym%20management%20system%20project%20-%20ClickJacking%20exists%20on%20multiple%20pages.assets/image-20220812165121053.png)



# Link

https://www.sourcecodester.com/php/15515/gym-management-system-project-php.html