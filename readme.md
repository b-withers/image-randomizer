<h1>Random Hero Image on refresh</h1>

<p>On a website I was developing, I wanted to have a random "Hero" image displayed each time the page was refreshed. What I thought would be a simple solution turned out to be a little more involved than I thought. Here is my solution! </p>

<br>

<ul>
<li>HTML</li>
<li>CSS</li>
<li>jQuery</li>
<li>Bootstrap</li>
</ul>

<br>

<p>I put the function inside the HTML, but it could easily be moved to a external file. An array of images is created, and then called randomly and displayed to the specified class, easy peasy<p>

```java
<!--Function to randomly pick an image from array-->
    <script type="text/javascript">
        $(function() {
            //array of images, I named them in numerical order for simplicty
            var images = ['1.jpg', '2.jpg', '3.jpg', '4.jpg', '5.jpg', '6.jpg', '7.jpg', '8.jpg'];
            //jQuery function contains path to images, and function to call a random image, please note the url is the correct path to your images!
            $('.hero').css({'background-image': 'url(img/backgrounds/' + images[Math.floor(Math.random() * images.length)] + ')'});
            });
    </script>
```

<img src="/img/readme/random.gif">