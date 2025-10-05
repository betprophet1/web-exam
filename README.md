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