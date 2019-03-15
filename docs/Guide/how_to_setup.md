**1. Website Set-Up**

#**Prerequisite**

Xampp

Clone this Repo directly into xampp/htdocs path.

![screenshot_2019-02-26 xinfinorg tradefinexlive](https://user-images.githubusercontent.com/22572604/53394517-8d17d280-39c5-11e9-875c-510792592022.png)

#**Front End**

Go to - application/config.php

Set - $config['base_url'] = 'http://example.com/' or 'https://example.com/'

![ss2](https://user-images.githubusercontent.com/22572604/53398863-ae31f080-39d0-11e9-9c6c-4c293bfa2220.png)

Go to - application/database.php

Set -
'hostname' => 'localhost', (change required if needed)
'username' => '',
'password' => '',
'database' => '',

![ss3](https://user-images.githubusercontent.com/22572604/53399063-2ef0ec80-39d1-11e9-8f1a-f29c38c1d422.png)

Go to - application/emailc.php

Set -

$config['$econfig'] = array('protocol' => 'smtp',

'smtp_host' => '', /* email gateway host /

'smtp_port' => 465,

'smtp_user' => '', / email gateway username /

'smtp_pass' => '', / email gateway password */

'wordwrap' => TRUE,

'charset' => 'utf-8');

![ss4](https://user-images.githubusercontent.com/22572604/53399233-9444dd80-39d1-11e9-8cb1-87b9e948066b.png)


#**Admin Panel**

Go to - application/adminpanel/config.php

Set - $config['base_url'] = 'http://example.com/adminpanel/' or 'https://example.com/adminpanel/'

![ss5](https://user-images.githubusercontent.com/22572604/53400806-a5dbb480-39d4-11e9-9efd-165507ee1d2e.png)


Go to - application/adminpanel/constants.php

Set to - define('BASE_FRONT_URL', 'http://example.com/' or 'https://example.com/');

![ss6](https://user-images.githubusercontent.com/22572604/53404917-ac6e2a00-39dc-11e9-9dea-463783a8bdc8.png)

Go to - application/adminpanel/database.php

Set to -

'hostname' => 'localhost', (change required if needed)

'username' => '',

'password' => '',

'database' => '',

![ss7](https://user-images.githubusercontent.com/22572604/53493055-74d8ae00-3ac0-11e9-8da4-b632c1619ba5.png)



