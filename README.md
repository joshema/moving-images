
Stack Overflow
Products
CSS Animation that moves continually
Asked 8 years, 2 months ago
Modified 8 years, 2 months ago
Viewed 1k times

0


I have a CSS animation which i have created which simulates water travelling down a tunnel. It uses only one image which i also created. The animation works but doesnt move smoothly. I want the animation to continually move from right to left where the animation has a fixed width of say 500/600px.

Heres the code I have so far:

@-moz-keyframes waves{
    0%{
        left:0
    }

    100%{
        left:-580px
    }

}



body{
    background:#e6e6e5;
    overflow:hidden
}

.waves{
    position:fixed;
    bottom:0;   
    width:640px;
    z-index:0;
    opacity:0.75
}

.waves .wave{
    left: 150px;
    position:absolute;
    width:1200px;
    height:100px;
    background-image:url(images/flow.png);
    background-repeat:repeat-x
}

.waves .wave.bottom-wave{
    -moz-animation:waves 10s infinite linear;
    -webkit-animation:waves 17s infinite linear;
    animation:waves 10s infinite linear;
    bottom:164px
}

<html>
   <body>
      <div class="waves">           
       <div class="wave bottom-wave"></div>
      </div>
   </body>
</html>
