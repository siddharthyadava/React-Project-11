# 📘 React useMemo Example – Performance Optimization Demo

This project demonstrates how to optimize expensive computations in a React component using useMemo.
The example shows the difference between normal rendering and memoized value computation by preventing unnecessary recalculations of a heavy function.

## 🚀 Features

🔹 Uses React Hooks (useState, useMemo)

🔹 Includes a simulated expensive computational task

🔹 Prevents re-execution of heavy logic unless required

🔹 Demonstrates performance optimization in React

## 🧠 How It Works
1. expensiveTask()

A dummy heavy function that runs a loop up to 1,000,000,000 to simulate costly processing.

function expensiveTask(num) {
  console.log("Inside Expensive Task");
  for(let i = 0; i <= 1000000000; i++) {}
  return num * 2;
}

2. useMemo

The result of the expensive function is memoized so it only runs when input changes.

let doubleValue = useMemo(() => expensiveTask(input), [input]);


Changing count does NOT recalculate the expensive task.

Changing input triggers recalculation.

## 📂 App Functionality

Increment Button: Updates a normal state (count)

Input Field: Enter a number to compute its double

Memoized Output: Shows the doubled value without re-running expensive code unnecessarily

## 💻 How to Run the Project
1. Clone or download the repository
git clone <your-repo-url>
cd your-project-folder

2. Install dependencies
npm install

3. Start the development server
npm start

4. View in browser
http://localhost:3000

## 📦 Project Structure
/src
  ├── App.js
  ├── App.css
  └── index.js