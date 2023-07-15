# Q.1  Whats React and its pros and cons?

React.js is one of the most popular front-end JavaScript libraries for building Web applications. It is actively maintained by Meta and a community of skilled developers and companies. It is known to be fast, scalable, simple, and highly advantageous to be used to create large web applications where we can change data without reloading the page. 

Pros of React:

Allows building reusable and modular components.
Provides efficient rendering with virtual DOM.
Supports unidirectional data flow for easier debugging.
Has a large community and ecosystem for support and resources.

Cons of React:

Initial learning curve to understand React concepts.
Can involve complex tooling and configuration
Requires using JSX syntax, which may be unfamiliar to some.
May have a slight performance overhead compared to direct DOM manipulation.
Advanced state management may require additional learning and integration.

# Q.2 What do you understand by Virtual Dom?

The Virtual DOM (Virtual Document Object Model) is a concept and technique used by React and other JavaScript libraries/frameworks to optimize the performance of updating and rendering user interfaces. It is an abstraction of the actual browser DOM, a representation of the HTML structure of a web page.This approach enables the declarative API of React: You tell React what state you want the UI to be in, and it makes sure the DOM matches that state. This abstracts out the attribute manipulation, event handling, and manual DOM updating that you would otherwise have to use to build your app.

# Q.3 Difference between Virtual Dom vs Real Dom.

Real Dom:-
1. DOM manipulation is very expensive.
2. There is too much memory wastage.
3. It updates Slow.
4. It can directly update HTML.
5. Creates a new DOM if the element updates.

Virtual Dom:-
1. DOM manipulation is very easy.
2. No memory wastage.
3. It updates fast.
4. It can’t update HTML directly It can’t update HTML directly .
5. Update the JSX if the element update.

# Q.4 Whats component? Types of component.

A component is a self-contained, reusable building block that encapsulates a portion of the user interface (UI) and its behavior. Components allow developers to break down complex UIs into smaller, modular parts, making the code more organized, maintainable, and reusable.

1.Functional Components:

Functional components are defined as JavaScript functions.
They receive props (input data) as arguments and return the UI representation based on those props.
They are primarily responsible for presenting the data and do not maintain their own internal state.
Functional components are simpler and easier to test and reason about.
With the introduction of React Hooks in React 16.8, functional components gained the ability to handle state and lifecycle through the useState and useEffect hooks.

2.Class Components :

Class components are defined as JavaScript classes that extend the React.Component class.
They have their own internal state managed by React.
Class components can receive props and have lifecycle methods like componentDidMount, componentDidUpdate, etc.
They are suitable for complex components that require state management and lifecycle hooks.

# Q.5 Difference between class & function based component.

Class-based Components:
- Defined using classes in JavaScript.
- Can manage component state and use lifecycle methods.
- More verbose syntax and can be complex.
- Used in older React codebases.
- Provides an object-oriented approach.

Function-based Components:
- Defined using regular functions.
- Don't have lifecycle methods (before Hooks).
- Simpler and shorter syntax.
- Promotes functional programming style.
- Preferred approach with the introduction of Hooks.
- Offers improved reusability and testability.

# Q.6 Explain react component life cycle.

In React, component lifecycle refers to the series of phases a component goes through from its initialization to unmounting. Each phase provides specific opportunities for performing actions such as initializing state, fetching data, or cleaning up resources. With the introduction of React Hooks, some lifecycle methods are replaced by equivalent hooks. 

the component lifecycle in React:
1. Initial Phase:
- Component is created and initialized.
- State and event handlers are set up in the constructor() method.

2. Mounting Phase:
- Component is rendered and inserted into the DOM.
- JSX markup is generated in the render() method.
- componentDidMount() is called after rendering, used for additional setup tasks.

3. Updating Phase:
- Occurs when component's props or state change.
- componentDidUpdate() is called after updates are reflected in the DOM.
- shouldComponentUpdate() determines if the component should re-render, optimizing   performance.

4. Unmounting Phase:
- Component is being removed from the DOM.
- componentWillUnmount() is called before unmounting, used for cleanup tasks.

# Q.7 Explain Prop Drilling in React & Ways to avoid it.

Prop drilling in React refers to the process of passing down props through multiple intermediate components that do not need the props themselves, but only serve as a conduit for passing the props to deeper components. It can occur when components that are not direct parents or children need access to certain props. Prop drilling can lead to code redundancy, decreased maintainability, and can make it harder to track and manage props across the component tree.

Avoiding Prop Drilling:
1. Context API: Utilize React's Context API to share data without explicitly passing props through intermediate components. Context provides a way to access shared data at any level of the component tree without the need for manual prop passing.
2. State management libraries: Implement state management libraries like Redux or MobX to centralize the application state. These libraries allow components to access the required data without relying on prop drilling.
3. React Hooks: Leverage React Hooks such as `useContext` or custom hooks to manage shared state within functional components. This reduces the need for prop drilling by allowing components to directly access and modify shared state.
4. Component composition: Break down the UI into smaller, more focused components to minimize the need for prop drilling. By organizing components effectively, you can keep the flow of data localized and reduce the propagation of props through unnecessary levels.
5. Higher-order components (HOCs) or render props: Utilize HOCs or render props pattern to inject necessary data directly into components that need it, instead of passing it through intermediate components.