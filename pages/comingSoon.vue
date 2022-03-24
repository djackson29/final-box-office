<template>
<div class="comingSoon">
  <h1>Coming Soon to Theaters</h1>

  <!-- accordion -->
  <div class="accordion" role="tablist">

    <!-- accordion 1 is open by default -->
    <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block v-b-toggle.accordion-1 variant="info">March 25</b-button>
      </b-card-header>
      <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">

        <!-- accordion body uses v-for to grab data from week 1 object -->
        <b-card-body>
          <div v-for="week1 in week1Movies" v-bind:key="week1.id">
            <div class="row">
              <div class="col">
                <h3><em>{{ week1.name }}</em></h3>
                <b-card-text>{{ week1.genre }}</b-card-text>
                <b-card-text>{{ week1.summary }}</b-card-text>
              </div>
              <div class="col">
                <img v-bind:src="week1.img" class="cs-img">
              </div>
            </div>
          </div>
  </b-card-body>
  </b-collapse>
  </b-card>

  <!-- accordion 2 is closed by default -->
  <b-card no-body class="mb-1">
    <b-card-header header-tag="header" class="p-1" role="tab">
      <b-button block v-b-toggle.accordion-2 variant="info">April 1</b-button>
    </b-card-header>
    <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">

      <!-- accordion body uses v-for to grab data from week 2 object -->
      <b-card-body>
        <div v-for="week2 in week2Movies" v-bind:key="week2.id">
          <div class="row">
            <div class="col">
              <h3><em>{{ week2.name }}</em></h3>
              <b-card-text>{{ week2.genre }}</b-card-text>
              <b-card-text>{{ week2.summary }}</b-card-text>
            </div>
            <div class="col">
              <img v-bind:src="week2.img" class="cs-img">
            </div>
          </div>
        </div>
</b-card-body>
</b-collapse>
</b-card>

<!-- accordion 3 is closed by default -->
<b-card no-body class="mb-1">
  <b-card-header header-tag="header" class="p-1" role="tab">
    <b-button block v-b-toggle.accordion-3 variant="info">April 8</b-button>
  </b-card-header>
  <b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">

    <!-- accordion body uses v-for to grab data from week 3 object -->
    <b-card-body>
      <div v-for="week3 in week3Movies" v-bind:key="week3.id">
        <div class="row">
          <div class="col">
            <h3><em>{{ week3.name }}</em></h3>
            <b-card-text>{{ week3.genre }}</b-card-text>
            <b-card-text>{{ week3.summary }}</b-card-text>
          </div>
          <div class="col">
            <img v-bind:src="week3.img" class="cs-img">
          </div>
        </div>
      </div>
    </b-card-body>
  </b-collapse>
</b-card>
</div>
</div>
</template>


<!-- Add "scoped"attribute to limit CSS to this component only -->
<script scoped>
// created object for each week, includes movie names, summaries, and genre(s)
export default {
  name: 'comingSoon',
  data() {
    return {

      // week 1 object
      week1Movies: [{
          name: "Infinite Storm",
          summary: 'When a climber gets caught in a blizzard, she encounters a stranded stranger and must get them both down the mountain before nightfall.',
          genre: 'Drama, Thriller',
          img: 'https://m.media-amazon.com/images/M/MV5BOTlkNTA4NWUtYzVkZC00NTIzLTk4ODEtY2RjYjAwMmZhYzQxXkEyXkFqcGdeQXVyMTM1MTE1NDMx._V1_SX300.jpg'
        },
        {
          name: "Everything Everywhere All at Once",
          summary: 'An aging Chinese immigrant is swept up in an insane adventure, where she alone can save the world by exploring other universes connecting with the lives she could have led.',
          genre: 'Action, Adventure, Comedy, Family, Sci-Fi',
          img: 'https://m.media-amazon.com/images/M/MV5BYTdiOTIyZTQtNmQ1OS00NjZlLWIyMTgtYzk5Y2M3ZDVmMDk1XkEyXkFqcGdeQXVyMTAzMDg4NzU0._V1_SX300.jpg'
        },
        {
          name: "The Lost City",
          summary: 'A reclusive romance novelist on a book tour with her cover model gets swept up in a kidnapping attempt that lands them both in a cutthroat jungle adventure.',
          genre: 'Action, Adventure, Comedy, Romance',
          img: 'https://m.media-amazon.com/images/M/MV5BMmIwYzFhODAtY2I1YS00ZDdmLTkyYWQtZjI5NDIwMDc2MjEyXkEyXkFqcGdeQXVyODk4OTc3MTY@._V1_SX300.jpg'
        }
      ],

      // week 2 object
      week2Movies: [{
          name: "Barbarians",
          summary: 'A dinner party in a country house that sees four friends come together for a birthday celebration. But as the night progresses secrets emerge and unsettling events begin to unfold around them.',
          genre: 'Thriller',
          img: 'https://m.media-amazon.com/images/M/MV5BY2ViNmFjM2QtMTIzNS00NzJhLTkxYjItYjNhZGQyZjZjYWI3XkEyXkFqcGdeQXVyMjM4NTM5NDY@._V1_SX300.jpg'
        },
        {
          name: "The Contractor",
          summary: 'A discharged U.S. Special Forces sergeant, James Harper, risks everything for his family when he joins a private contracting organization.',
          genre: 'Action, Thriller',
          img: 'https://m.media-amazon.com/images/M/MV5BYzZlYWIwMGMtYzgxYS00MTAyLWEzMjQtODIyZWM4ZTM5NzU3XkEyXkFqcGdeQXVyMzMwOTU5MDk@._V1_SX300.jpg'
        }
      ],

      // week 3 object
      week3Movies: [{
          name: "Ambulance",
          summary: "Two robbers steal an ambulance after their heist goes awry.",
          genre: 'Action, Comedy, Thriller',
          img: 'https://m.media-amazon.com/images/M/MV5BYjUyN2VlZGEtNGEyZC00YjViLTgwYmQtZDJiM2FlOTU3Mjg2XkEyXkFqcGdeQXVyMjMxOTE0ODA@._V1_SX300.jpg'
        },
        {
          name: "Cow",
          summary: 'A close-up portrait of the daily lives of two cows.',
          genre: 'Documentary',
          img: 'https://m.media-amazon.com/images/M/MV5BZDlhOWE5ODktNmVmZi00MzUyLTgzZDctMjVhNDhhYzk4NDE2XkEyXkFqcGdeQXVyNjU0NTI0Nw@@._V1_SX300.jpg'
        },
        {
          name: "Aline",
          summary: 'With the support of her family and the man she loves, the 14th child of a modest family will become the most famous singer in the world.',
          genre: 'Biography, Comedy, Drama, Music',
          img: 'https://m.media-amazon.com/images/M/MV5BNjUxYTQ3YzItNjU5Ny00ZGM0LWJkMGUtN2FkMWRiNjFlY2ExXkEyXkFqcGdeQXVyMzcwMzExMA@@._V1_SX300.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.card-body {
    background-color: #E0E8F9;
    border: none;
}

.cs-img {
    max-height: 150px;
}
</style>
