# How to Delete an Item From an Array With Vanilla JavaScript

**Author:** gomakethings.com  
**Full title:** How to Delete an Item From an Array With Vanilla JavaScript  
**URL:** https://gomakethings.com/how-to-delete-an-item-from-an-array-with-vanilla-javascript/  
**Source:** #articles #instapaper #readwise

- Using the Array.splice() method 
   
- The Array.splice() method accepts three arguments: start, delete, and items 
   
- The second, delete, is the number of items to delete from the array. If you omit this argument, the Array.splice() method will remove every item from the start index on 
   
- The Array.splice() method modifies the original array. If you want, you can duplicate it before modifying using the Array.from() method. 
   
- let fewerWizards = Array.from(wizards);
  fewerWizards.splice(1, 1); 
   
- The Array.splice() method returns the removed item, so you can’t create the new array, splice it, and assign it to a variable in one line. 
   
- Deleting an item by name instead of index 
   
- If you’re not sure what the index of the item you want to delete is, you can use the Array.indexOf() method to find it first. 
   
- let start = wizards.indexOf('Radagast');
  wizards.splice(start, 1); 
   
- Using the Array.filter() method 
   
- The Array.filter() method creates a new array with only elements that pass a test you include as a callback function 
   
- The callback accepts three arguments: the current item in the loop’s value, its index, and the array itself. 
   
- let fewerWizards = wizards.filter(function (wizard, index) {
  return index !== 1;
  }); 
   
- You can also remove the item by its value like this. 
   
- let fewerWizards = wizards.filter(function (wizard) {
  return wizard !== 'Radagast';
  }); 
   
- Which one should you use? 
   
- If you know the index of the item and want to modify the existing array, I would use Array.splice() 
   
- If you don’t have the index, or if you want to leave the original unmodified, I think Array.filter() is the better choice. 
   
