# [:house: Feni Batch Home Page](http://poloey.github.io/feni)

# Class 32 
# Isotope
go to https://isotope.metafizzy.co/ website and add isotope js file in your html file.   
write markup for isotope
~~~html
<div class="grid">
  <div class="grid-item web">...</div>
  <div class="grid-item atom">...</div>
  <div class="grid-item city">...</div>
</div>
~~~

initialize isotope plugin with jquery. [dependancy jquery]
~~~js
$grid = $('.grid').isotope({
  // options
  itemSelector: '.grid-item',
  layoutMode: 'fitRows'
});
~~~
filtering with isotope:     
write markup for filtering 
~~~html
<div>
  <button data-sumon='*' class="btn btn-info">all</button>
  <button data-sumon='.web' class="btn btn-info">Web</button>
  <button data-sumon='.server' class="btn btn-info">Server</button>
  <button data-sumon='.atom' class="btn btn-info">Atom</button>
</div>
~~~
make a onclick handler for click event. and get the selected button value and filter using isotope function
~~~js
$('button').on('click', function () {
  $value = $(this).attr('data-sumon');
  $grid.isotope({ filter: $value });
})
~~~
Thats all







# autoloading in php
