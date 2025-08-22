# TypeScript Quick Notes

---

## 1. What is the use of the keyof keyword in TypeScript? Provide an example.

In TypeScript, `keyof` is an operator that converts all keys of an object type into a union type.

### Example:

```ts
type Person = {
  name: string;
  age: number;
  isStudent: boolean;
};

type PersonKeys = keyof Person;

// Now PersonKeys becomes: "name" | "age" | "isStudent"

```
## 2. Provide an example of using union and intersection types in TypeScript.
### 1. Union Type

### Example:

```ts
type ID = string | number;

let userId: ID;

userId = 101;       
userId = "U-2025";  
```
### 2. Intersection Type
### Example:
```ts
 type Person = {
  name: string;
  age: number;
}

type Employee = {
  employeeId: number;
  department: string;
}

// Intersection
type EmployeeProfile = Person & Employee;

const emp: EmployeeProfile = {
  name: "Dipto",
  age: 22,
  employeeId: 101,
  department: "Web Development"
};
```
