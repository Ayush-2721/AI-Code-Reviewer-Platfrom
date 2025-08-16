🔍 Issues:
* ❌ **Undeclared Variables**: The variables `a` and `b` are used within the function `sum` but are not declared or
passed as parameters. This will lead to a `ReferenceError` in strict mode or rely on global variables in non-strict
mode, which is highly discouraged and can lead to unpredictable behavior.
* ❌ **Lack of Modularity**: The function relies on external state (`a` and `b` in the global scope) rather than
accepting inputs directly. This makes the function less reusable, testable, and harder to understand its dependencies.

✅ Recommended Fix:

```javascript
function sum(a, b) {
return a + b;
}
```

💡 Improvements:
* ✔ **Function Parameters**: By taking `a` and `b` as parameters, the function becomes self-contained and operates only
on the inputs provided.
* ✔ **Modularity & Reusability**: The `sum` function can now be used anywhere with any two numbers without relying on
external variables, making it highly reusable and predictable.
* ✔ **Predictable Behavior**: The function's output now solely depends on its inputs, making it easier to reason about
and debug.

---
**Final Note:** Always define or pass variables as parameters to functions to ensure they are self-contained,
predictable, and reusable. Avoiding reliance on global variables is a fundamental best practice for clean and
maintainable code.