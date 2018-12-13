[under construction]

# React Philosophy
 I think the smoothest way to deal with some tech is to understand minds of its creators.. With what principles they keep in mind while creating it and to much extend they stayed loyal to these principles.. There are few principles and many rules that supports/derived from them.. So, unless we don't feel and assimilate the principles, it is more likely we deal with bugs as we move forward, since rules will start not to make sense as things to deal with get advanced.. Luckily, react team shares what they have in their mind.. So lets just read and amaze the work they did with react :)

 ## Composition of React Components


"React has a powerful composition model, and we recommend using composition instead of inheritance to reuse code between components. Developers new to React often reach for inheritance, and show how we can solve them with composition.


Containment: Some components don’t know their children ahead of time. This is especially common for components like Sidebar or Dialog that represent generic “boxes”.
We recommend that such components use the special children prop to pass children elements directly into their output.
This lets other components pass arbitrary children to them by nesting the JSX. While this is less common, sometimes you might need multiple “holes” in a component. In such cases you may come up with your own convention instead of using children.


Specialization: Sometimes we think about components as being “special cases” of other components. In React, this is also achieved by composition, where a more “specific” component renders a more “generic” one and configures it with props.


Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way. If you want to reuse non-UI functionality between components, we suggest extracting it into a separate JavaScript module. The components may import it and use that function, object, or a class, without extending it.
 "

Composition Patterns
 "Lifting State & Container/Presenter: Divide components into stateful “containers” and stateless “presenters”.
Pass functions (“callbacks”) that change the container state as props to children
If two components need access to the same state, move the state into their common parent
Often, several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor. 

Higher-Order Component (HOC): A higher-order component is a function that takes a component and returns a component.
Think of an HOC as a component factory or a stage in a “component assembly line”.
A higher-order component (HOC) is an advanced technique in React for reusing component logic. HOCs are not part of the React API, per se. They are a pattern that emerges from React’s compositional nature.
Whereas a component transforms props into UI, a higher-order component transforms a component into another component.
Components are the primary unit of code reuse in React. However, you’ll find that some patterns aren’t a straightforward fit for traditional components.
Note that a HOC doesn’t modify the input component, nor does it use inheritance to copy its behavior. Rather, a HOC composes the original component by wrapping it in a container component. A HOC is a pure function with zero side-effects.


Render Prop/Function-as-Child: Components that use the “render prop” pattern invert control of rendering from the component itself to the consumer by accepting the render function as a prop. This prop is commonly called “render”, although since JSX children are turned into the 3rd argument to createElement, the children prop can be repurposed as a render prop, too (the function-as-child pattern).
The term “render prop” refers to a technique for sharing code between React components using a prop whose value is a function.
A component with a render prop takes a function that returns a React element and calls it instead of implementing its own render logic.
Components are the primary unit of code reuse in React, but it’s not always obvious how to share the state or behavior that one component encapsulates to other components that need that same state.
More concretely, a render prop is a function prop that a component uses to know what to render.
One interesting thing to note about render props is that you can implement most higher-order components (HOC) using a regular component with a render prop. 



“Renderless” State Provider: The “renderless” component pattern takes the container-presenter pattern to the extreme and forces state management to be implemented completely separately from render logic.
 "


# References
- [Design Principles](https://reactjs.org/docs/design-principles.html)
- [Fiber Architecture](https://github.com/acdlite/react-fiber-architecture)
- [Composition vs Inheritance](https://reactjs.org/docs/composition-vs-inheritance.html)
- [React Composition Patterns From The Ground Up](https://hackernoon.com/react-composition-patterns-from-the-ground-up-8401aaad93d7)
- [Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)
- [Higher Order Components](https://reactjs.org/docs/higher-order-components.html)
- [Render Props](https://reactjs.org/docs/render-props.html)
  
