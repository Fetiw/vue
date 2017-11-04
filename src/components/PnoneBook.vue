<template>
  <div>
    <phone-filter @filter="change"></phone-filter>

    <ul>
      <li v-for="phone in filteredPhones">
        <p class="name">{{phone.name}}</p>
        <p class="phone">{{phone.phone}}</p>
      </li>
    </ul>
  </div>
</template>

<script>
  import PhoneFilter from './PhoneFilter'

  export default {
    components: { PhoneFilter },
    name: 'phone-book',
    data () {
      return {
        filter: '',
        phones: [
          { phone: '554 54545645 54', name: 'test' },
          { phone: '123 54545645 54', name: 'tset' },
          { phone: '554 54545645 51', name: 'test1' }
        ]
      }
    },
    methods: {
      change: function (filter) {
        this.filter = filter
      }
    },
    computed: {
      filteredPhones () {
        return this.phones.filter((phone) => {
          return (
            phone.name.indexOf(this.filter) !== -1 ||
            phone.phone.indexOf(this.filter) !== -1
          )
        })
      }
    }
  }
</script>