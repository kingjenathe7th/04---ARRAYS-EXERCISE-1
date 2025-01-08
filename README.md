**JavaScript Array Methods Examples**
=====================================

**Overview**
------------

This repository contains a collection of examples demonstrating the use of various JavaScript array methods, including `filter()`, `map()`, `sort()`, and `reduce()`. The examples are designed to illustrate the functionality of these methods and provide a starting point for further exploration.

**Examples**
------------

### 1. Filtering Inventors by Birthdate

*   **Method:** `filter()`
*   **Description:** Filter the list of inventors to include only those born in the 1500s.
*   **Code:**

    ```javascript
    const fifteen = inventors.filter(inventor => (inventor.year >= 1500 && inventor.year < 1600));
    ```

### 2. Mapping Inventor Names

*   **Method:** `map()`
*   **Description:** Create an array of inventor full names.
*   **Code:**

    ```javascript
    const fullnames = inventors.map(inventor => `${inventor.first} ${inventor.last}`);
    ```

### 3. Sorting Inventors by Birthdate

*   **Method:** `sort()`
*   **Description:** Sort the list of inventors by birthdate in ascending order.
*   **Code:**

    ```javascript
    const oldest = inventors.sort((a, b) => a.year > b.year ? 1 : -1);
    ```

### 4. Calculating Total Years Lived by Inventors

*   **Method:** `reduce()`
*   **Description:** Calculate the total number of years lived by all inventors.
*   **Code:**

    ```javascript
    const totalYearsLived = inventors.reduce((total, inventor) => {
        return total + (inventor.passed - inventor.year);
    }, 0);
    ```

### 5. Sorting Inventors by Years Lived

*   **Method:** `sort()`
*   **Description:** Sort the list of inventors by the number of years they lived in descending order.
*   **Code:**

    ```javascript
    const oldestInventor = inventors.sort((a, b) => {
        const lastInventor = a.passed - a.year;
        const nextInventor = b.passed - b.year;
        return lastInventor > nextInventor ? -1 : 1;
    });
    ```

### 6. Filtering Paris Boulevards

*   **Method:** `filter()`
*   **Description:** Create a list of Paris boulevards that contain the string "de".
*   **Note:** This example requires access to a Wikipedia page containing a list of Paris boulevards.

### 7. Sorting People by Last Name

*   **Method:** `sort()`
*   **Description:** Sort the list of people by last name in ascending order.
*   **Code:**

    ```javascript
    const sortedPeople = people.sort((lastOne, nextOne) => {
        const [aLast, aFirst] = lastOne.split(', ');
        const [bLast, bFirst] = nextOne.split(', ');
        return aLast > bLast ? 1 : -1;
    });
    ```

### 8. Counting Transportation Modes

*   **Method:** `reduce()`
*   **Description:** Count the occurrences of each transportation mode in the provided data.
*   **Code:**

    ```javascript
    const transportation = data.reduce((obj, item) => {
        if (!obj[item]) {
            obj[item] = 0;
        }
        obj[item]++;
        return obj;
    }, {});
    ```

**Getting Started**
-------------------

1.  Clone the repository to your local machine.
2.  Open the `index.js` file in your preferred code editor.
3.  Run the code using Node.js or a JavaScript runtime environment.

**Contributing**
--------------

Contributions are welcome! If you'd like to add more examples or improve existing ones, please submit a pull request.

**License**
----------

This repository is licensed under the MIT License.