# oslab9

1)options of chown and gpasswd

 a)chown:

Chown -R:

تغییر مالکیت فایل به صورت بازگشتی_ برای اینکه به صورت بازگشتی روی 
کلیه ی فایل ها و دایرکتوری های یک دایرکتوری مشخص کار کنید

Chown -H: 

اگر آرگومان های ارسالی به دستور یک فایل اشاره گر باشد که به یک دایرکتوری
اشاره می کند این گزینه باعث می شود که دستور آن فایل را بپیماید

Chown -L:

هر فایل اشاره گری را تا دایرکتوری اشاره شده می پیماید 

gpasswd:

-a: 
اضافه کردن کاربر به گروه

-r: 
پاک کردن پسورد گروه

-d:
ریموو کردن کاربر از گروه 

2)name UID GID

cat /etc/ passwd

 
 اطلاعات کامل کاربری در فایل
  
etc/passwd

ذخیره می‌شوند این فایل برای هر یوزر موجود در سیستم یک رکورد دارد
 پس باید این فایل را بخوانیم در فیلد های

GUID  و  UID

میتوانیم شناسه کاربر و گروه را ببینیم

3)creating user oslab and set password 25

اول با استفاده از دستور یوزر اد کاربر مورد نظر را ایجاد میکنیم
سپس با دستور مربوط به پسورد  پسورد ۲۵ را برای ان ست میکنیم 

sudo useradd oslab

sudo passwd oslab

سپس از ما میخواهد که یک پسورد وارد کنیم و ما 25 را وارد میکنیم

4)
با دستور گروپ اد گروه های سجاد و یونی را ایجاد میکنیم سپس با استفاده
از دستور اد یوزر به انها کاربر مورد نظر را به هر دو گروه اضافه میکنیم 

sudo groupadd sajjad

sudo groupadd uni

sudo adduser oslab sajjad

sudo adduser oslab uni

sudo gpasswd -A oslab sajjad

gpasswd -A :
کاربر مورد نظر را ادمین میکند

5)
ابتدا با دستور یوزر اد کاربر را ایجاد میکنیم سپس آن را عضو گروه سجاد 
میکنیم  

sudo useradd os2

sudo gpasswd -a os2 sajjad

این دستور کاربر را به گروه اد میکند

sudo userdel os2

این دستور کاربر را پاک می‌کند 



