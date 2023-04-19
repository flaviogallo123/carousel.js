
let slideIndex = 1;
showSlides(slideIndex);

function plusSlides2(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}    
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
}







 

let slideIndex2 = 0;
let timeoutId = null;
const slides = document.getElementsByClassName("mySlides2");
const dot = document.getElementsByClassName("dot");

showSlides2();
function currentSlide(index) {
     slideIndex = index;
     showSlides2();
}
function plusSlides(step) {
  
  if(step < 0) {
      slideIndex2 -= 2;
      
      if(slideIndex2 < 0) {
        slideIndex2 = slides.length - 1;
      }
  }

  showSlides2();
}
function showSlides2() {
  for(let i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
    dot[i].classList.remove('active');
  }
  slideIndex2++;
  if(slideIndex2 > slides.length) {
    slideIndex2 = 1
  }
  slides[slideIndex2 - 1].style.display = "block";
  dot[slideIndex2 - 1].classList.add('active');
   if(timeoutId) {
      clearTimeout(timeoutId);
   }
  timeoutId = setTimeout(showSlides2, 5000); // Change image every 5 seconds
}






let slideIndex3 = 0;
let timeoutId3 = null;
const slides3 = document.getElementsByClassName("mySlides3");
const dot3 = document.getElementsByClassName("dot");

showSlides3();
function currentSlide(index) {
     slideIndex3 = index;
     showSlides3();
}
function plusSlides3(step) {
  
  if(step < 0) {
      slideIndex3 -= 2;
      
      if(slideIndex3 < 0) {
        slideIndex3 = slides3.length - 1;
      }
  }

  showSlides3();
}
function showSlides3() {
  for(let i = 0; i < slides3.length; i++) {
    slides3[i].style.display = "none";
    dot[i].classList.remove('active');
  }
  slideIndex3++;
  if(slideIndex3 > slides3.length) {
    slideIndex3 = 1
  }
  slides3[slideIndex3 - 1].style.display = "block";
  dot[slideIndex3 - 1].classList.add('active');
   if(timeoutId3) {
      clearTimeout(timeoutId3);
   }
  timeoutId3 = setTimeout(showSlides2, 5000); // Change image every 5 seconds
}












