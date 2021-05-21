What is React.js
    - React.js is a library for handling our UI. It allows us to write reuseable code when needed.

Why would you use React.js
    - The fact that React.js components allow us to reuse bits of our code means that work can be done so much quicker. I think it's amazing?

What are components
    - Components are independent and reusable bits of code.

What is JSX
    - stands for JavaScript XML. JSX allows us to write HTML in React. JSX makes it easier to write and add HTML in React.

What are props
    - props are arguments we pass into components to differentiate them. 

What is state
    - state is where we store stuff related to the component. when the state object changes, the component reacts and re-renders.

What are the differences btw/ functional and class based components
    - Class components are used as container components to handle state management and wrap child components. Functional components generally are just used for display purposes - these components call functions from parent components to handle user interactions or state updates

Give an example of a functional and class based component
    - Functional

        const PageOne = () => {
        return (
            <h1>Page One</h1>
         );
    }

    - Class Based

        class App extends Component {
            render () {
                return (
                    <Text>Hello World!</Text>
                )
            }
        }

What are React Hooks
    - Hooks are the new feature introduced in the React 16.8 version. It allows you to use state and other React features without writing a class. Hooks are the functions which "hook into" React state and lifecycle features from function components.

How does useState work
    - Hooks are the new feature introduced in the React 16.8 version. It allows you to use state and other React features without writing a class. Hooks are the functions which "hook into" React state and lifecycle features from function components The useState Hook allows you to declare only one state variable (of any type) at a time useState takes the initial value of the state variable as an argument. The initial value will be assigned only on the initial render (if it’s a function, it will be executed only on the initial render). In subsequent renders (due to a change of state in the component or a parent component), the argument of the useState Hook will be ignored and the current value will be retrieved.

Give an example of useState
    - function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}