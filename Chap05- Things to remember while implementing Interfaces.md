## Things to remember while implementing Interfaces

1. Use the C# interfaces when you need to implement the same methods in more than one script, or when you need to reference an unknown class in the same context
2. Interface members don't have access to modifiers, as they are all public.
3. The name of an interface must be a valid C# identifier name. By convention, interface names begin with a capital ” I ”
4. C# is an interface may define default implementations for some or all of its members. A class or struct that implements the interface doesn't have to implement members that have default implementations. For more information, see default interface methods.
5. An interface can't be instantiated directly. Its members are implemented by any class or struct that implements the interface

