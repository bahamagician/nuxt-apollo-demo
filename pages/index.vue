<template>
  <div>
    <div v-for="blog in blogs">
      {{ blog.title }}
    </div>
  </div>
</template>

<script>
import gql from 'graphql-tag'

export default {
    apollo: {
      blogs: gql`{
        blogs {
          title
          body
        }
      }`,
    }
}
</script>
