# Website Development Project 01

Fullpage scroll without using Fullpage.js


# Source Information

index.html : main body
style.css : main css stylesheet
main.js : simple javascript

# Version

ver0.1 -  Pure HTML/CSS version - CSSOM Scroll-behavior
          not supporting some browsers like Safari
          refer to the following website
          https://caniuse.com/?search=scroll-behavior

ver0.2 -  jQuery implementation <br>
<p><code>
$('.navbar a').on('click', function (e) {
.navbar a : select the parameter
.on('click') : choose event
function(e) : event function
    if (this.hash !== '') {
If this 'hash' is not EMPTY, we have to prevent the default action.
        e.preventDefault();

        const hash = this.hash;
make 'hash' a variable.

        $('html, body').animate({
             scrollTop: $(hash).offset().top
choose the 'scrollTop method
 choose 'hash' and offset
         }, 800); //set the speed for 800 mili-seconds

    }
 });
</code></p>


