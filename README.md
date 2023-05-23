# Clickable-Column
Elementor Clickable Column Section Container


<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script>
var $ = jQuery
$(document).ready(function(){
    
$('.elementor-section[link], .elementor-column[link] > .elementor-widget-wrap, .e-con[link], .e-container[link]').on('click', function(){
    
    var $this = $(this).hasClass('elementor-widget-wrap') ? $(this).parent() : $(this),
    link = $this.attr('link'),
    newtab = $this.attr('newtab'),
    openIn = typeof newtab !== 'undefined' && newtab !== false ? '_blank' : '_self'
    
    window.open(link, openIn)
})
})
</script>
<style>
.elementor-section[link], .elementor-column[link] > .elementor-widget-wrap, .e-con[link], .e-container[link] {
    cursor: pointer;
}
</style>
