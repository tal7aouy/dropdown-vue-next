# dropdown-vue

An easier way to display A Vue.js dropdown component,
No special dependencies, no jquery, no tailwind.css, just VueJS and CSS magic.

# Installation

```bash
$ npm install dropdown-vue-next
// OR
$ yarn add  dropdown-vue-next
```

# Requirements

- [Vue.js](https://github.com/vuejs/vue-next) `^3.0.0`

# Usage

```html
<Dropdown
  :options="arrayOfObjects"
  :selected="object"
  @updateOption="onSelectedOption"
  :placeholder="'Select your Option'"
  :closeOnOutsideClick="boolean"
>
</Dropdown>

<script setup>
  import Dropdown from 'dropdown-vue-next'
  import {reactive, ref} from 'vue
  const countries = ref([
      {id:1, name:'Morocco'},
      {id:2, name:'USA'},
      {id:3,name: "Canada"}
    ])
  let object = reactive({name: "Object Name"})

  const onSelectedOption = (payload) => object = payload
</script>
```

# Default values of props

| Property            |  Type   |       Default value |
| ------------------- | :-----: | ------------------: |
| closeOnOutsideClick | boolean |                true |
| placeholder         | string  | 'Select an option.' |

# License

[The MIT License](http://opensource.org/licenses/MIT)
