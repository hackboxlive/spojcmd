spojcmd  (Rachit Nimavat)
=========================


Config File (optional)
---------------
	Create a file named .spojcmdrc  in your home folder, with the following  contents -

	[user]
	user_name = YOUR_USERNAME
	password = YOUR_PASSWORD
	wait_time = 4	(time interval in seconds for querying status of your submission)
	pyver = 2.7	(version for python compiler - 2.7 / 3.2.3 / nbc )
	cppver = 4.3.2	(version for gcc cpp compiler - 4.3.2 / 4.0.0.0-8 )
	cver = 4.3.2	(version for gcc c compiler - 4.3.2 / 99 )
	pasver = fpc	(version for pascal compiler - fpc / gpc )

	Note that, all these options are optional except [user] section line


Setup Instructions
--------------

First, get python-pip. Then install spojcmd by it. Resolve unsatisfied dependencies, if any.

    >sudo apt-get install python-pip
    >sudo pip install spojcmd


Login to SPOJ
---------------

Login to SPOJ like this:

	>spojcmd login <username>
	>password: <password>


User Stats
---------------------

To get any user's solved/unsolved problems:
	>spojcmd status <username>

For your own stats:
	>spojcmd stats
	


Бодлого илгээх
--------------

`tackle` коммандаар бодлогоо илгээнэ, үүний тулд кодын файлын нэрээ
аргументэд нь өгнө. Кодын файлын нэр бодлогын дугаарыг, өргөтгөл нь 
тухайн бодлогыг ямар хэл дээр шийдсэнийг илэрхийлнэ. 
Жишээ нь:

	>spoj tackle problem_id.c


Бодлогууд
---------

`list' коммандаар нийт бодологуудын жагсаалтыг харах боломжтой. Мөн баганы
дугаараар хүснэгтийн эрэмбэлэх боломжтой.
Жишээ нь:

    >spoj list --page=2 --sort=1


Бодлогын дэлгэрэнгүй
--------------------
`desc` коммандаар бодлогын дэлгэрэнгүйг харна. Үүнд бодлогын өгүүлбэр болон,
жишээ оролт, гаралтын утгууд агуулагдана. Мөн зөвхөн жишээ оролт эсвэл
гаралтын утгыг авах боломжтой.

    >spoj desc problem_id # дэлгэрэнгүй мэдээлэл
    >spoj desc --input problem_id # зөвхөн жишээ оролтын утга
