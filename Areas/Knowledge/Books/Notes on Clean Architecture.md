
# Notes on Clean Architecture
- Creation Date: <% 2024-9-20 %>
- Last Update: <% 2024-9-13 %>
- Tags / Categories: #reading 
- State: 🌱
- Type: 
- Author: Robert C. Martin
- Type: Books
- Genre: #learning #coding 
- Related: 
- Started reading: 2024-09-20
- Current page: 49/373
- Finished reading: 
- Origin:
> [!summary]
> 
> In this document we will summarize and analyze this books contents, taking into account what we can extract from the book to our daily development.

## Notes During Reading
- "The measure of design quality is simply the measure of the effort required to meet the needs of the customer. If that effort is low, and stays low throughout the lifetime of the system, the design is good. If that effort grows with each new release, the design is bad. It’s as simple as that."
- "To fulfill its purpose, software must be soft—that is, it must be easy to change. When the stakeholders change their minds about a feature, that change should be simple and easy to make. The difficulty in making such a change should be proportional only to the scope of the change, and not to the shape of the change."
- Structured Programming:
	- The first paradigm to be adopted (but not the first to be invented) was structured programming, which was discovered by Edsger Wybe Dijkstra in 1968. Dijkstra showed that the use of unrestrained jumps (goto statements) is harmful to program structure. As we’ll see in the chapters that follow, he replaced those jumps with the more familiar if/then/else and do/while/until constructs. We can summarize the structured programming paradigm as follows:
		- Structured programming imposes discipline on direct transfer of control.
- Object-Oriented Programming
	- The second paradigm to be adopted was actually discovered two years earlier, in 1966, by Ole Johan Dahl and Kristen Nygaard. These two programmers noticed that the function call stack frame in the ALGOL language could be moved to a heap, thereby allowing local variables declared by a function to exist long after the function returned. The function became a constructor for a class, the local variables became instance variables, and the nested functions became methods. This led inevitably to the discovery of polymorphism through the disciplined use of function pointers. We can summarize the object-oriented programming paradigm as follows:
		- Object-oriented programming imposes discipline on indirect transfer of control.
- Functional Programming
	- The third paradigm, which has only recently begun to be adopted, was the first to be invented. Indeed, its invention predates computer programming itself. Functional programming is the direct result of the work of Alonzo Church, who in 1936 invented l-calculus while pursuing the same mathematical problem that was motivating Alan Turing at the same time. His l-calculus is the foundation of the LISP language, invented in 1958 by John McCarthy. A foundational notion of l-calculus is immutability—that is, the notion that the values of symbols do not change. This effectively means that a functional language has no assignment statement. Most functional languages do, in fact, have some means to alter the value of a variable, but only under very strict discipline. We can summarize the functional programming paradigm as follows:
		- Functional programming imposes discipline upon assignment.
- Conclusion
	- What does this history lesson on paradigms have to do with architecture? Everything. We use polymorphism as the mechanism to cross architectural boundaries; we use functional programming to impose discipline on the location of and access to data; and we use structured programming as the algorithmic foundation of our modules. Notice how well those three align with the three big concerns of architecture: function, separation of components, and data management.
- Dependency Inversion
	- With this approach, software architects working in systems written in OO languages have absolute control over the direction of all source code dependencies in the system. They are not constrained to align those dependencies with the flow of control. No matter which module does the calling and which module is called, the software architect can point the source code dependency in either direction.
	- What can you do with that power? As an example, you can rearrange the source code dependencies of your system so that the database and the user interface (UI) depend on the business rules (Figure 5.3), rather than the other way around.
	- This means that the UI and the database can be plugins to the business rules. It means that the source code of the business rules never mentions the UI or the database.