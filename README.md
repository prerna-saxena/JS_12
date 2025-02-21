# JS_12
JS_12

Borrowing a method
function hash(args) {
  return args[0] + ',' + args[1];
}

 arr.join method: TO JOIN ARRAYS

function hash(args) {
  return args.join();
}

function hash() {
  alert( [].join.call(arguments) ); // 1,2
}

hash(1, 2);
The trick is called method borrowing.

We take (borrow) a join method from a regular array ([].join) and use [].join.call to run it in the context of arguments.

Taken from the specification almost “as-is”:

Let glue be the first argument or, if no arguments, then a comma ",".
Let result be an empty string.
Append this[0] to result.
Append glue and this[1].
Append glue and this[2].
…Do so until this.length items are glued.
Return result.

Decorators and function properties
----------------------------------------
a decorator may count how many times a function was invoked and how much time it took, 
and expose this information via wrapper properties.
There exists a way to create decorators that keep access to function properties, b
ut this requires using a special Proxy object to wrap a function. 

A proxy object is a wrapper around another object (called the target) that intercepts and controls interactions with that object. It allows you to customize or augment the default behavior of the target object, such as property access, assignment, and method invocation.

Decorator is a wrapper around a function that alters its behavior. The main job is still carried out by the function.

func.call(context, arg1, arg2…) – calls func with given context and arguments.
func.apply(context, args) – calls func passing context as this and array-like args into a list of arguments.





 
