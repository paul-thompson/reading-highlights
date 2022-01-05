# Custom Right Click Context Menu With jQuery

**Author:** Yogesh Singh  
**Full title:** Custom Right Click Context Menu With jQuery  
**URL:** https://makitweb.com/custom-right-click-context-menu-with-jquery/  
**Source:** #articles #instapaper #readwise

- When right-clicking on the element then disable the browser default context menu and display the custom options 
   
- // disable right click and show custom context menu
  $("h2").bind('contextmenu', function (e) {
  var id = this.id;
  $("#txt_id").val(id);
  var top = e.pageY+5;
  var left = e.pageX;
  // Show contextmenu
  $(".context-menu").toggle(100).css({
  top: top + "px",
  left: left + "px"
  });
  // disable default context menu
  return false;
  }); 
   
- Hide context menu when to click or right-click outside 
   
- Bind contextmenu and click event on the document to hide the custom menu and remove the hidden field id. 
   
- $(document).bind('contextmenu click',function(){
  $(".context-menu").hide();
  $("#txt_id").val("");
  }); 
   
- Disable default menu from custom context menu 
   
- // disable context-menu from custom menu
  $('.context-menu').bind('contextmenu',function(){
  return false;
  }); 
   
