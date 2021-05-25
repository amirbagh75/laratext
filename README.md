<div dir='rtl'>

# LaraText | لاراتکست

![main](https://user-images.githubusercontent.com/21690865/119399353-06f6ad80-bcee-11eb-8730-8377d2344b17.gif)
    
این پروژه با اهداف آموزشی برای [بوت‌کمپ داکر هلدینگ گرین‌وب](https://evnd.co/l2PJx) ایجاد شده است.
به‌وسیله این پروژه میتوانید تصاویر دارای متون فارسی/انگلیسی را به کمک موتور OCR به نام [Tesseract](https://google.com)  به رشته متنی تبدیل کنید.


نحوه استفاده از پروژه در حالت غیر داکری:

</div>

```shell
root@pc:~$ git clone https://github.com/amirbagh75/laratext laratext
root@pc:~$ cd laratext
root@pc:~$ composer install
root@pc:~$ php8.0 artisan laratext:convert
```

<div dir='rtl'>

با زدن دستور بالا، آدرس تصویر را از شما میپرسد که کافیست آدرس مطلق فایل را به آن پاس دهید و منتظر چاپ رشته متنی باشید.

---

نحوه استفاده از پروژه در حالت داکری:
 
</div>

```shell
root@pc:~$ git clone https://github.com/amirbagh75/laratext laratext
root@pc:~$ cd laratext
root@pc:~$ docker build -t laratext -f Dockerfile-cli .
root@pc:~$ docker run --name laratext --interactive --tty --rm laratext
```

<div dir='rtl'>

---

همچنین میتوانید پروژه را به صورت مستقیم از داکر‌هاب نیز دریافت و اجرا کنید:

</div>

```shell
root@pc:~$ docker run --name laratext -it --rm amirbagh75/laratext:cli
```

<div dir='rtl'>

---

همچنین این پروژه دارای نسخه وب‌اپلیکیشن نیز میباشد. برای مثال میتوانید نسخه داکری‌ آن را به وسیله وب‌سرور داخلی PHP، بدین‌شکل اجرا کنید:

</div>

```shell
root@pc:~$ docker run --name laratext --rm -p 8080:8000 amirbagh75/laratext:cli serve --host 0.0.0.0
```

<div dir='rtl'>

یا اگر قصد دارید در محیط‌های پروداکشنی استفاده کنید، میتوانید نسخه با وب‌سرور آپاچی آن را اجرا کنید:

</div>

```shell
root@pc:~$ docker run --name laratext --rm -p 8080:8000 amirbagh75/laratext:apache
```

<div dir='rtl'>

سپس کافیست در مرورگر خود وارد آدرس `127.0.0.1:8080` شوید.

</div>
