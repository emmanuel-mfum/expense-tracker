# expense-tracker
Expense tracker by year and month designed with React

The goal of this project was to understand the basics upon which React is build on ; namely, JavaScrpit ES6 syntax, React components,
React state, listening to events (clicks or changes on a component), dynamically rendering lists and rendering components or code
conditionally.

The result is this SPA (single-page application) that can keep track of expenses by year and can display the proportion of the amounts 
of money spent across the different months of the year over the total amount spent in the year in a chart.

The user can add new expenses, but they won't be saved as this is a front-end only application for now.

To add an expense simply click on the "Add New Expense" button:

![image](https://user-images.githubusercontent.com/55893421/115976758-396e8880-a53f-11eb-8b71-6d931aafe7dd.png)

This will trigger the appearance of a form that the user can fill thanks to the use of a boolean state variable.
Once the user is done, he can click on "Add Expense" or he can change his mind and click on "Cancel" which will remove the chart
from the screen. If the new expense is added, it will be added to a list of already-existing "dummy" entries which is in fact a array of JS objects.

These objects will then be handled by the logic of the application for a dynamic rendering where each object is mapped (using the JS function "map()")
into a React component. The already exisiting (and rendered) array is then updated with the new entries for expenses and displayed on the screen.

If a particular year doesn't have any expenses recorded, then we conditionally render ( the condition being that no entries for expenses are recorded
for that year) the text "Found no expenses". 

For the chart, the logic behind it, is that we loop across all the items (expenses recorded) of  a year and calculate the total.
Then we compare the amount spent each month with the total recorded for the year (the proportion over the total) and depending on that 
ratio we color the columns corresponding to each month accordingly.

View the demo here : https://emmanuel-mfum.github.io/expense-tracker/
