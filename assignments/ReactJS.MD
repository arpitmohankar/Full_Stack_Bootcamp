# ReactJS Foundational Problems

## 1. Break Down the UI into Components  

Take a look at the provided UI. Your task is to divide it into multiple React components. You don't need to write any code for this step. Simply use a pen and paper or a photo editing tool to visualize how the UI can be split into different components. This exercise will help you get a better understanding of component structure in React.


![UI Image](https://github.com/smaranjitghose/Full_Stack_Bootcamp/blob/f681b71e60c357846a377f94de394bb16859beef/assignments/zerodha_components.png)

## 2. Create a Greet Component
 
- Create a new file called `Greet.jsx` and inside that file, write a `Greet` component using the **function declaration** syntax.
- Afterward, refactor the `Greet` component to use the **arrow function** syntax.
- Finally, register the `Greet` component in your `App.jsx` file so that you can see the result when running the app.



## 3. Rendering Multiple Components and Nesting Components

Step 1: Create a Header Component

1. Create a new file called `Header.jsx`.
2. Inside this file, create a functional component named `Header`.
3. The `Header` component should return a `<header>` element with the following:
   - A `<h1>` element with the text "Welcome to My Portfolio!"
   - A `<nav>` element containing three links (`<a>`) with the text "Home", "About", and "Contact"

Step 2: Create a Footer Component

1. Create a new file called `Footer.jsx`.
2. Inside this file, create a functional component named `Footer`.
3. The `Footer` component should return a `<footer>` element with a `<p>` containing the text "© 2025 Your Name"

Step 3: Create a MainContent Component

1. Create a new file called `MainContent.jsx`.
2. Inside this file, create a functional component named `MainContent`.
3. The `MainContent` component should return a `<main>` element containing:
   - A `<h2>` element with the text "Main Content"
   - A `<p>` element with any text of your choice

 Step 4: Render Components Inside App.jsx

1. In your `App.jsx` file, import the `Header`, `MainContent`, and `Footer` components:
   ```jsx
   import Header from "./Header";
   import MainContent from "./MainContent";
   import Footer from "./Footer";
   ```

2. Inside the `App` component's return statement, render the three components inside a single `<div>`, in the following order:
   - `Header`
   - `MainContent`
   - `Footer`

Your `App.jsx` should look like this:
```jsx
function App() {
  return (
    <div>
      <Header />
      <MainContent />
      <Footer />
    </div>
  );
}

export default App;
```


## 4. Understanding JSX

#### Step 1: Create a New Component

1. Create a new file called `WelcomeMessage.jsx`.
2. Inside this file, write a functional component called `WelcomeMessage`.
3. The component should return a `<div>` that contains:
   - A `<h1>` element that displays the message: `"Hello, World!"`
   - A `<p>` element that displays the message: `"Welcome to learning JSX!"`

#### Step 2: Render the Component in App.jsx

1. Open the `App.jsx` file.
2. Import the `WelcomeMessage` component at the top of the file:
3. Inside the `App` component's return statement, render the

#### Step 3: Run the Application

1. Run the app in your development environment.
2. You should see the `"Hello, World!"` message along with `"Welcome to learning JSX!"` displayed in your browser.


## 5. JSX Rules


#### Step 1: Create a New Component

1. Create a new file called `JSXRules.jsx`.
2. Inside this file, write a functional component called `JSXRules`.

The component should return a `<div>` containing the following:

- A `<h1>` element with the text `"JSX Rules"`.

- A paragraph (`<p>`) that lists at least 3 rules of JSX:
  - JSX must return a **single parent element**.
  - JSX elements must be **properly closed**.
  - JSX attributes are written using **camelCase** (e.g., `className` instead of `class`).


## 6. JSX Expressions 

#### Step 1: Create a `Greeting` Component

1. Create a new file called `Greeting.jsx`.
2. Inside this file, create a functional component named `Greeting`.
3. The `Greeting` component should return a `<div>` containing:

   - A `<h1>` element that dynamically displays a greeting message.
   - A `<p>` element that dynamically displays the current date.

4. Use JavaScript expressions inside `{}` to dynamically render the following:
   - A `name` variable containing a name, such as `"John"`.
   - A `new Date()` object to display the current date.

#### Step 2: Create a `ProductInfo` Component

1. Create a new file called `ProductInfo.jsx`.
2. Inside this file, create a functional component named `ProductInfo`.
3. The `ProductInfo` component should return a `<div>` that dynamically displays product details:

   - Use a `product` object that contains the following properties:
     - `name`: `"Laptop"`,
     - `price`: `$1200`,
     - `availability`: `"In stock"`

4. Display the product name, price, and availability using `{}`.

#### Step 3: Render Components in `App.jsx`

1. In your `App.jsx` file, import the `Greeting` and `ProductInfo` components:

   ```jsx
   import Greeting from "./Greeting";
   import ProductInfo from "./ProductInfo";
   ```

2. Inside the `App` component's return statement, render both components:

   ```jsx
   function App() {
     return (
       <div>
         <Greeting />
         <ProductInfo />
       </div>
     );
   }

   export default App;
   ```

## 7. Displaying a list of data


#### Step 1: Create a `UserList` Component

1. Create a new file called `UserList.jsx`.
2. Inside this file, create a functional component called `UserList`.
3. In the component, create a `users` array with the following objects, where each object represents a user with `id`, `name`, and `age`:

   ```javascript
   const users = [
     { id: 1, name: "Alice", age: 25 },
     { id: 2, name: "Bob", age: 30 },
     { id: 3, name: "Charlie", age: 22 },
   ];
   ```

4. Use the `.map()` method to render a list of users. Each user's `name` and `age` should be displayed inside a `<div>` element. Use the `id` as the unique `key` for each list item.

#### Step 2: Create a `ProductList` Component

1. Create a new file called `ProductList.jsx`.
2. Inside this file, create a functional component called `ProductList`.
3. Create a `products` array with the following objects, where each object represents a product with `id`, `name`, and `price`:

   ```javascript
   const products = [
     { id: 1, name: "Phone", price: "$699" },
     { id: 2, name: "Laptop", price: "$1200" },
     { id: 3, name: "Headphones", price: "$199" },
   ];
   ```

4. Use the `.map()` method to render the list of products. Each product’s `name` and `price` should be displayed inside a `<div>` element. Use the `id` as the `key` for each product.

#### Step 3: Render the Components in `App.jsx`

1. In your `App.jsx` file, import the `UserList` and `ProductList` components:

   ```jsx
   import UserList from "./UserList";
   import ProductList from "./ProductList";
   ```

2. Inside the `App` component's return statement, render both the `UserList` and `ProductList` components:

   ```jsx
   function App() {
     return (
       <div>
         <UserList />
         <ProductList />
       </div>
     );
   }

   export default App;
   ```


## 8. Passing Props to Components

#### Step 1: Create a `Person` Component

1. Create a new file called `Person.jsx`.
2. Inside this file, create a functional component called `Person`.
3. This component should accept `props` and render:

   - A `<h2>` element that displays the person's name.
   - A `<p>` element that displays the person's age.

4. Use `props.name` and `props.age` to display the dynamic values passed from the parent component.

#### Step 2: Create a `Product` Component

1. Create a new file called `Product.jsx`.
2. Inside this file, create a functional component called `Product`.
3. This component should accept `props` and render:

   - A `<h2>` element that displays the product's name.
   - A `<p>` element that displays the product's price.

4. Use `props.name` and `props.price` to display the values passed from the parent component.

#### Step 3: Pass Props from `App.jsx`

1. In your `App.jsx` file, import the `Person` and `Product` components:

   ```jsx
   import Person from "./Person";
   import Product from "./Product";
   ```

2. Inside the `App` component, pass dynamic data as props to both `Person` and `Product` components:
   - Pass `name` and `age` as props to the `Person` component.
   - Pass `name` and `price` as props to the `Product` component.


## 9. Prop Destructuring

In this exercise, you will learn how to use **destructuring** to simplify how you access props in React components.

#### Step 1: Create a `Person` Component with Props Destructuring

1. Create a new file called `Person.jsx`.
2. Inside this file, create a functional component called `Person`.
3. Destructure the `name` and `age` props directly in the function parameters and render:
   - A `<h2>` element that displays the person's name.
   - A `<p>` element that displays the person's age.

#### Step 2: Create a `Product` Component with Props Destructuring

1. Create a new file called `Product.jsx`.
2. Inside this file, create a functional component called `Product`.
3. Destructure the `name` and `price` props in the function parameters and render:
   - A `<h2>` element that displays the product's name.
   - A `<p>` element that displays the product's price.

#### Step 3: Pass Props from `App.jsx`

1. In your `App.jsx` file, import the `Person` and `Product` components:

   ```jsx
   import Person from "./Person";
   import Product from "./Product";
   ```

2. Inside the `App` component, pass the `name` and `age` props to the `Person` component, and `name` and `price` props to the `Product` component.

Example:

```jsx
function App() {
  return (
    <div>
      {/* Passing props to Person */}
      <Person name="John Doe" age={28} />
      <Person name="Jane Smith" age={32} />

      {/* Passing props to Product */}
      <Product name="Laptop" price="$1200" />
      <Product name="Smartphone" price="$699" />
    </div>
  );
}

export default App;
```


