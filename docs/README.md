<link rel="stylesheet" href=".css/w3.css">

<script>
    var TxtRotate = function(el, toRotate, period) {
        this.toRotate = toRotate;
        this.el = el;
        this.loopNum = 0;
        this.period = parseInt(period, 10) || 2000;
        this.txt = '';
        this.tick();
        this.isDeleting = false;
    };

    TxtRotate.prototype.tick = function() {
        var i = this.loopNum % this.toRotate.length;
        var fullTxt = this.toRotate[i];

        if (this.isDeleting) {
            this.txt = fullTxt.substring(0, this.txt.length - 1);
        } else {
            this.txt = fullTxt.substring(0, this.txt.length + 1);
        }

        this.el.innerHTML = '<span class="wrap">'+this.txt+'</span>';

        var that = this;
        var delta = 300 - Math.random() * 100;

        if (this.isDeleting) { delta /= 2; }

        if (!this.isDeleting && this.txt === fullTxt) {
            delta = this.period;
            this.isDeleting = true;
        } else if (this.isDeleting && this.txt === '') {
            this.isDeleting = false;
            this.loopNum++;
            delta = 500;
        }

        setTimeout(function() {
            that.tick();
        }, delta);
    };

    window.onload = function() {
        var elements = document.getElementsByClassName('txt-rotate');
        for (var i=0; i<elements.length; i++) {
            var toRotate = elements[i].getAttribute('data-rotate');
            var period = elements[i].getAttribute('data-period');
            if (toRotate) {
                new TxtRotate(elements[i], JSON.parse(toRotate), period);
            }
        }
        // INJECT CSS
        var css = document.createElement("style");
        css.type = "text/css";
        css.innerHTML = ".txt-rotate > .wrap { border-right: 0.08em solid #666 }";
        document.body.appendChild(css);
    };
</script>

<style>
    .ryuuganime {
        background: #ed3446;
        color: #ffffff;
    }

    .ryuuganime:hover {
        color: #000000;
    }
</style>

<h1 style="text-align:center;">
  <span
     class="txt-rotate"
     data-period="2000"
     data-rotate='[ "Hello, and welcome to Ryuuganime Docuwiki!", "Halo, dan selamat datang di Ryuuganime Docuwiki!", "اهلا وسهلا و مرحبا بكم الى ريوغانيمي دوكوويكي!", "こんにちは、リュウガニメ•ドクウィキへようこそ!" ]'></span>
</h1>
<br/>

<!-- tabs:start -->
## **English (US)**
Welcome to Ryuuganime Docuwiki!

To getting started, please click this button to proceed into English version of this site.

[<span class="w3-button w3-round-large ryuuganime">Proceed to English version</span>](/en_US/)

## **Bahasa Indonesia**
Selamat datang di Ryuuganime Docuwiki!

Untuk memulai, silakan tekan tombol berikut untuk melanjutkan ke versi Bahasa Indonesia.

[<span class="w3-button w3-round-large ryuuganime">Lanjutkan ke versi Bahasa Indonesia</span>](/id_ID/)

<!-- tabs:end -->