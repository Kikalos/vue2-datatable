<template>
  <a href="javascript:;" @click="handleClick" style="padding-left: 5px" name="HeadSort">
    <i :class="cls"></i>
  </a>
</template>
<script>
/**
 * Sorting arrows within <th>
 */
export default {
  props: {
    field: { type: String, required: true },
    query: { type: Object, required: true }
  },
  data: () => ({
    order: ''
  }),
  computed: {
    cls () {
      return [
        'fa',
        `fa-sort-${this.order}`.replace(/-$/, ''),
        { 'text-muted': !this.order }
      ]
    }
  },
  watch: {
    query: {
      handler ({ sort: field, order }) {
        this.order = field === this.field ? order : ''
      },
      deep: true,
      immediate: true
    }
  },
  methods: {
    handleClick () {
      const { query, order } = this
      query.sort = this.field
      query.order = this.order = order === 'desc' ? 'asc' : 'desc'
    }
  }
}
</script>
