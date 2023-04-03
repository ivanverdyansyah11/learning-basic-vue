<template>
  <section>
    <div class="row justify-content-center text-start">
      <div class="col-8">
        <div class="row">
          <div class="col-12 mb-4 d-flex justify-content-between align-items-center">
            <h2 class="fw-semibold">{{ title }} Practice</h2>
            <button v-on:click="practiceName" class="btn btn-primary btn-sm">Practice name</button>
          </div>
          <div class="col-12">
            <div class="input-group mb-3">
              <input type="text" class="form-control" placeholder="Search student.." aria-describedby="button-addon1" v-model="searchStudent">
              <button class="btn btn-outline-secondary" type="button" id="button-addon1">Search</button>
            </div>
            <p>result: {{ searchStudent }}</p>
          </div>
          <div class="col-12">
            <table class="table">
            <thead>
              <tr class="table-dark">
                <th scope="col">No</th>
                <th scope="col">Fullname</th>
                <th scope="col">Origin</th>
                <th scope="col">Passion</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="student in studentMachine" :key="student.id">
                <td>{{ student.id }}</td>
                <td>{{ student.fullname }}</td>
                <td>{{ student.origin }}</td>
                <td>{{ student.passion }}</td>
              </tr>
            </tbody>
          </table>
          <div class="col-12 mt-5">
            <div class="wrapper d-flex gap-1">
              <a v-bind:href="urlMiawaug" class="btn btn-danger btn-sm">YT. Miauwaug</a>
              <a v-bind:href="urlZahidIbrahim" class="btn btn-danger btn-sm">YT. Zahid Ibrahim</a>
              <a v-bind:href="urlDeddyCorbuzier" class="btn btn-danger btn-sm">YT. Deddy Corbuzier</a>
              <a v-bind:href="urlTemaIndonesia" class="btn btn-danger btn-sm">YT. Tema Indonesia</a>
            </div>
          </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      'title': 'Data Binding',
      'students': [],
      'urlMiawaug': 'https://www.youtube.com/@Miawaug',
      'urlZahidIbrahim': 'https://www.youtube.com/@zahidibr',
      'urlDeddyCorbuzier': 'https://www.youtube.com/@corbuzier',
      'urlTemaIndonesia': 'https://www.youtube.com/@TemaIndonesiaProduction',
      'searchStudent' : ''
    }
  },
  methods: {
    practiceName() {
      this.title = 'Computed Properties'
    },
  },
  mounted() {
    this.students = [
        {id: 1, fullname: 'Aditya Prayatna', origin: 'Bali, North Denpasar', passion: 'Programming'},
        {id: 2, fullname: 'Ayu Nanda', origin: 'Bali, West Denpasar', passion: 'Graphic Design'},
        {id: 3, fullname: 'Agus Prayoga', origin: 'Bali, Gianyar', passion: 'Athletic'},
        {id: 4, fullname: 'Dimas Putra', origin: 'Bali, South Denpasar', passion: 'Photograph'},
      ]
  },
  computed: {
    studentMachine() {
      return this.students.filter((item) => {
        return item.fullname.match(this.searchStudent)
      })
    }
  }
}
</script>