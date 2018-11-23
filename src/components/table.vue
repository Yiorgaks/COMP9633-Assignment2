<template>
  <table class="table">
    <thead>
      <tr>
        <th>Title</th>
        <th>Subtitle</th>
        <th>Body</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="row in rows" class="active">
        <td>{{ row.title }}</td>
        <td>{{ row.subtitle }}</td>
        <td>{{ row.body }}</td>
      </tr>
    </tbody>
  </table>
</template>

  <script>
    export default {
      name: "gbc-table",
    props: ["rows"]
  };
</script>
