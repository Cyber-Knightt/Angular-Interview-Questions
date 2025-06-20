# Table of Contents

<!-- TOC_START -->
| No. | Questions |
| --- | --------- |
| 1 | [Describe the architecture of a scalable Angular application you've built?](#Describe the architecture of a scalable Angular application you've built?) |
| 2 | [What is a prototype chain](#what-is-a-prototype-chain) |


<!-- TOC_END -->


<!-- QUESTIONS_START -->
1. ### Describe the architecture of a scalable Angular application you've built?

**A scalable Angular app uses:**

  
•	Modular architecture with core, shared, feature, and lazy-loaded modules.

•	Smart/dumb component separation (container vs presentational).

•	State management with services or libraries like NgRx.

•	Lazy loading to split bundles and reduce initial load time.

•	Reusable UI libraries with shared components, directives, and pipes.

•	Strict linting and TypeScript types to catch issues early.


      **[⬆ Back to Top](#table-of-contents)**

2. ### What is a prototype chain

   **Prototype chaining** is used to build new types of objects based on existing ones. It is similar to inheritance in a class based language. i.e, When you create an object using a constructor function or a class, the created object inherits properties from a prototype object.

   The prototype on object instance is available through **Object.getPrototypeOf(object)** or **\_\_proto\_\_** property whereas prototype on constructor function is available through **Object.prototype**.

   ![Screenshot](images/prototype_chain.png)

   **[⬆ Back to Top](#table-of-contents)**

3. ### What is closures

	A closure is a function that has been bundled together (enclosed) with references to its surroundings (the lexical environment). In other words, a closure allows an inner function to access the scope of an outside function. Closures are formed every time a function is created in JavaScript, during function creation time. An example of closures in Javascript is given below:

	```javascript
	function subtractor(subtractingInteger) {
		return function(a) {
			return a - subtractingInteger;
		};
	}

	var subtract2 = subtractor(2);
	var subtract5 = subtractor(5);
	console.log(subtract2(5));  // 3 is logged
	console.log(subtract5(5)); // 0 is logged
	```
	In this example, we have developed a function subtractor(subtractingInteger) that takes a single parameter subtractingInteger and returns a new function. Its return function accepts only one input, a, and returns the difference of a and subtractingInteger. The function 'subtractor' is essentially a function factory. It creates functions that have the ability to subtract a specified value from their arguments. The function factory creates two new functions in the example above: one that subtracts 2 from its argument and one that subtracts 5 from its arguments. Both subtract2 and subtract5 are closures. They have the same function body definition, but they hold lexical surroundings that are distinct. subtractingInteger is 2 in subtract2's lexical environment, but subtractingInteger is 5 in subtract5's lexical environment.

	**[⬆ Back to Top](#table-of-contents)**

---

## 🎯 Bonus Topics
- **Event Emitters**
- **Worker Threads**
- **Child Processes**
- **Cluster Module**
- **WebSockets**

---

This README serves as a roadmap. Practice regularly and build small projects to reinforce concepts.

---

_Updated: April 2025_

