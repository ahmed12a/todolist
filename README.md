# todolist
this a code for making a to do list. i am having trouble with the $ when i run my code on the console. if anyone can give me an insight where i am wrong it would be appreciated


let todolist = [];


function additem(arr) {
  let answer = prompt('what would you like to do today?');
  let correct = answer.toLowerCase().trim();



  if (checkduplicate(arr, correct)) {
    arr.push(correct);
    showitems(todolist);
  }
  else {
    alert('item already exists, do not work so hard');
  }
}

function checkduplicate(arr, item) {
  let isunique = false;
  let index = arr.indexOf(item);//-1

  if (index != -1) {
    isunique = false;
  }
  else {
    isunique = true;
  }
  return isunique;

}
//REMOVE ITEM FUNTION
function removeitem(list){
  let answer=prompt('which item would you like to delete from the list')
  let correct= answer.trim().toLowerCase();

  let index=list.indexOf(correct);

  if(!checkduplicate(list,correct)){
    let removeditem= list.splice(index,1);
    console.log(removeditem);
    alert('you removed "${removeditem}" frm your list');

  }
  else{
    console.log('no such value exists');
    
}

}

//function showitems
function showitems(list){
  let listvalues= "your list items are : ";

  for(let i = 0; i<list.length; i++){
    listvalues += '"list item nr${i+1}: ${list[i]}"'
  }
  alert(listvalues);
}
additem(todolist);
additem(todolist);
additem(todolist);
removeitem(todolist);
showitems(todolist);


console.log(todolist);
