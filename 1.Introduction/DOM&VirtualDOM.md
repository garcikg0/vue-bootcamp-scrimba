DOM
- Document Object Model (HTML & XML)
- Node Tree structure
- DOM Tree is great until you have to change bits and pieces. DOM changes are computationally expensive. The way Plain JavaScript (vanilla JavaScript) or jQuery works. 

We need a solution that performs changes to DOM quickly, optimizes DOM changes and change least amount of times, and remove tree traversing as much as posssible...

Virtual DOM
- Virtual DOM is an abstraction of the DOM (sits between Vue and DOM)
    - Uses custom JavaScript objects to represent elements (ex. plan or blueprint when building a house - changes in blueprints are quick & low-cost)
- Layer between Vue & the real DOM 

Virtual DOM to be in sync with DOM --> Patch, also known as DOM DIFFing, takes the list of changes from Vue that were applied to the Virtual DOM and applies it to the real DOM. These changes are stored as a Queue. And then we have a New DOM aka updated state. Process from patching to new updated state is called Tick. The tick is moving your clock one tick forward and updating the DOM one more time. 

Virtual DOM
- Patch is smart and complex. 
    - It removes any Vue-only code. 
    - Will sort smartly to not patch a node unnecessarily. 
    - Because it diffs, if the "change" yields the same result, nothing happens == no cost. 
    - This process is commonly known as DOM Diffing (Diff). Diff simply means to figure out what the differences are. 


