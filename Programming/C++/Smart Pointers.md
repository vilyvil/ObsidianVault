# Unique Pointer
A feature of the C++ standard library which owns a pointer to some object. Unique Pointers automatically dispose of their owned objects when they go out of scope. 

As their name implies, only one unique pointer can own a single object. The pointer cannot be copied into another variable. If this was possible, then when the object goes out of scope and is disposed of, the rest of the pointers would point at nothing.

# Shared Pointer
Shared pointers, unlike unique pointers, can own objects owned by other shared pointers. They keep track of how many other (in-scope) shared pointers point to an object. The object will only be disposed of once that count reaches 0.

### Caveat to shared_ptr
In some situations, shared pointers will own each other in a cycle. As a result, even when we leave the scope where they should all exist, the pointers are never disposed of, causing a memory leak. One way to fix this is making one connection in the cycle a weak_ptr.

# Weak Pointer
A smart pointer that holds a non-owning reference to an object that is already being managed by a shared pointer. Non-owning means that the original shared pointer count is not affected by the existence of a weak pointer. 

When all the shared pointers to an object are destroyed, that object is destroyed like normal. All of the weak pointers pointing to that object will expire.

Weak pointers can be converted to shared pointers, temporarily giving them ownership of the object and preventing it from being destroyed.