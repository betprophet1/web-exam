# Mini Debug - 15 to 20 mins

### Object/array reactivity 
Issue: Not reactive (new key + index set).

```
data() { 
  return { 
    profile: { 
      name: 'A'
    }, 
    items: ['a','b'] 
  } 
}
// later:
this.profile.age = 30
this.items[2] = 'x'
```

### Prop mutation 
Issue: Mutating prop directly.

```
props: { value: Boolean }
methods: {
  toggle() { this.value = !this.value }
}
```

### Watcher not firing on nested change
Issue: Shallow watch.

```
watch: {
  options(val) { /*...*/ } // expects deep nested changes
}
```

### Forwarding listeners/attrs in base component 
Issue: Parent @input doesn’t fire.

```
<!-- BaseInput.vue -->
<input v-bind="$attrs">
```

# Coding Exam

### Debounce function - 15 mins
- The debounced function should:
    - Wait until no calls happen for `delay` ms, then run fn.
    - If called again before `delay` ends, reset the timer.
- Must preserve the `this` context and arguments when executing `fn`.

```
function searchQuery(q) {
  console.log("Searching for:", q);
}

const debouncedSearch = debounce(searchQuery, 500);

// Simulate rapid calls
debouncedSearch("a");
debouncedSearch("ab");
debouncedSearch("abc");

// Expected behavior: Only logs once after 500ms:
// "Searching for: abc"
```


### Group Data By Key - 15 mins
- Accepts an array of objects.
- Groups items by the given property name.
- Returns an object where each key is the property value, and each value is an array of items.

```
const data = [
  { name: "Alice", role: "admin" },
  { name: "Bob", role: "user" },
  { name: "Charlie", role: "admin" },
  { name: "David", role: "user" }
];

const result = groupBy(data, "role");

console.log(result);
// Expected output:
// {
//   admin: [
//     { name: "Alice", role: "admin" },
//     { name: "Charlie", role: "admin" }
//   ],
//   user: [
//     { name: "Bob", role: "user" },
//     { name: "David", role: "user" }
//   ]
// }
```