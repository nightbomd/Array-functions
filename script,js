// Demo data array we will use in all examples
const foods = ['Pizza', 'Tacos', 'Ice Cream', 'Burgers', 'Pasta']


// helper function: will display whatever HTML/text we pass into the #out div
function render (html) {
  document.getElementById('out').innerHTML = html
}


/*
  1) listFoods()
     - Use a for...of loop
     - Output all foods into the #out div (as <p> tags or list items)
*/
function listFoods () {
 // render(`<p>${foods.map(food => `<p>${food}</p>`).join("")}</p>`);


  let output = "";
  for (const food of foods) {
    output += `<p>${food}</p>`;
  }
  render(output);
}


/*
  2) numberedFoods()
     - Use a classic for loop with index
     - Output foods as an ordered list (<ol><li>...</li></ol>)
*/
function numberedFoods () {
  // code goes here
  let output = `<ol class= "list-group list-group-numbered">`;


  for (let i = 0; i < foods.length; i++) {
     output += `<li class="list-group-item"> ${foods[i]}</li>`;
  }
  output += `</ol>`;
  render(output);
}


/*
  3) filterFoods()
     - Prompt the user for a letter
     - Loop through foods
     - Only show foods that start with that letter
     - If no matches, display a "not found" message
*/
function filterFoods () {
    const l = prompt("What letter cuh");
    if (!l) {
      prompt("nah cuh enter something cuh");
      return;
    }
    const filter = foods.filter(f => {
     return f.toLowerCase().startsWith(l.toLowerCase());
    })
    render(`<p>${filter.map(f => `<li class = "list-group-item">${f}</li>`).join(" ")}</p>`)
    if (filter.length === 0) {
      render(`<p> nah cuh it looks like u got no foods with that letter cuh</p>`);
    }
}


/*
  4) forEachFoods()
     - Use foods.forEach()
     - Output each food as a Bootstrap card
     - Cards should be placed in a centered row
*/
function forEachFoods () {
let output =  "<div class='row g-3 justify-content-center'>";
  foods.forEach((f) => {
    output += `<div class="col-3">
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">${f}</h5>
      </div>
    </div>
  </div>`;
  });
  render(output);
 


}


// ---- Event listeners (buttons) ----
document.getElementById('btnList').addEventListener('click', listFoods)
document.getElementById('btnNums').addEventListener('click', numberedFoods)
document.getElementById('btnFilter').addEventListener('click', filterFoods)
document.getElementById('btnForEach').addEventListener('click', forEachFoods)


//  ---------------STUDENT WORK SECTION--------------


/*
  Task 1 — Uppercase List
  -----------------------
  - Use .map() to create a new array with all foods in uppercase
  - Display the results as an unordered list (<ul>)
*/
function uppercaseList () {
  const coolList = foods.map(f => f.toUpperCase());
  render(`<p>${coolList.map(f => `<li class ="list-group-item">${f}</li>`).join("")}</p>`)
}


/*
  Task 2 — Reverse List
  ---------------------
  - Show the foods array in reverse order
  - You may use a backwards loop OR the built-in .reverse()
*/
function reverseList () {
  const k = foods.reverse();
  render(`<p>${k.map(f => `<li class ="list-group-item">${f}</li>`).join("")}</p>`)
}


/*
  Task 3 — Random Food Picker
  ---------------------------
  - Use Math.random to pick a random food from the array
  - Display it in a Bootstrap card with a heading like "Today's Pick"
*/
function randomFoodPicker () {
  const randomIndex = Math.floor(Math.random() * 5);
  const f = foods[randomIndex];
  render(`<p>${f}</p>`)
  return f;
}


/*
  Task 4 — Word Lengths


  ---------------------
  - Loop through each food in the array
  - Count the number of characters in each one
  - Display results in the format: Food — X letters
*/
function wordLengths () {
  let num = 0;
  for (let i = 0; i < foods.length; i++) {
    num += foods[i].trim().length;
  }
  render(`<p>there are ${num} letters cuh`);
}
const crazyFoods = () => {
  let storage = "";
  const intervalId = setInterval(() => {
    const nextFood = randomFoodPicker();
    storage += nextFood + " ";
    render(storage);
  }, -10000);
};
// ---- Event listeners for the new buttons ----
// (Make sure to add matching buttons in index.html)
document.getElementById('btnUppercase').addEventListener('click', uppercaseList)
document.getElementById('btnReverse').addEventListener('click', reverseList)
document.getElementById('btnRandom').addEventListener('click', randomFoodPicker)
document.getElementById('btnLengths').addEventListener('click', wordLengths)
