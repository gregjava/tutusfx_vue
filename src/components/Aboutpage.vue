<template>
  <v-app id="app">
    <v-container fluid class="row">
      <v-layout mainColumn>
        <v-flex class="card">
          <v-card class="segment"><br/>
            <h3>About Tutusfx</h3>
            <span
              v-for="item in articleBody" 
              :key="item.id" 
            ><br>
              <hr><p>{{ item.txt }}</p><hr><br>
            </span>
          </v-card>
        </v-flex>
      </v-layout>
      <v-layout rightColumn>
        <v-flex class="card">
          <v-card 
            v-for="item in AllPosts" 
            :key="item.id" 
            class="segment"
          ><br>
            <h3>{{ item.title }}</h3><hr>
            <h5><b> {{ item.desc }}</b></h5><br/><h6 class="rightAlign">{{ item.date }}</h6>
            <div class="imgholder largepicture">
              {{ item.img }}
            </div><hr>
            <p>{{ item.txt1 }}</p>
            <p>{{ item.txt2 }}</p><hr><br>
          </v-card>
          <v-card class="segment">
            <h3>Vote a Witness</h3><hr>
            <h4 class="leftAlign"><em>List of top witnesses</em></h4><br/>
            <p 
              v-for="item in witnessData" 
              :key="item.id"
            >
              {{ item.id }} {{ item.name }}
            </p>
            <p class="rightAlign">
              <a href="">More...</a>
            </p><br><br><hr><br>
          </v-card>
          <span class="returner">
            <a href="#"> Return to top </a>
          </span>
        </v-flex>
      </v-layout>
    </v-container>
  </v-app>
</template>
<script>
  export default {
    data: () => ({
      articleBody: [
        {
          txt: 'The threshold to create and operate a Marketing Network is quite high! Therefore, a one-stop solution is provided by the Tutusfx Community for anyone to create a unique Network without any thresholds. \nMeanwhile, with the help of TT Token Reward Mode, the operation threshold can be reduced effectively, with a short startup period. Cryptocurrency, currency and commodity instrument traders have traded for years without incentives or adequate motivation to match their passion for the trends. \nTutusfx presents a system that seeks to improve the analysis and trading of its instrument traders with relevant tools and incentives aimed at motivating traders and network operators, alike. \nIn view of the application experience in blockchain, Tutusfx Community comprises a bottom layer using a decentralized blockchain accounting-book to record the ownership information of trade products, and deal with the transaction of trade products by virtue of smart contracts so that the ecosystem economy of Network will be transparent and clear; while the application layer shall make use of efficient centric development architecture so as to fully guarantee the good performance of all read and write operations as well as to effectively avoid the problems of long confirmation duration, high cost and congestion-inducing, thus the smooth and interactive experience of Network products can be guaranteed at the extreme.'
        }
      ],
      AllPosts: [
        {
          title: 'Blockchain Post 3',
          desc: 'Title description',
          date: 'Dec 10, 2018',
          img: 'Image',
          txt1: 'Some text from Post 3...',
          txt2: 'Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.',
          views: '258',
          interactions: '14',
          comments: '5'
        },
        {
          title: 'Blockchain Post 2',
          desc: 'Title description',
          date: 'Nov 22, 2018',
          img: 'Image',
          txt1: 'Some text from Post 2...',
          txt2: 'Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.',
          views: '629',
          interactions: '73',
          comments: '18'
        },
        {
          title: 'Blockchain Post 1',
          desc: 'Title description',
          date: 'Nov 15, 2018',
          img: 'Image',
          txt1: 'Some text from Post 1...',
          txt2: 'Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.',
          views: '192',
          interactions: '9',
          comments: '4'
        }
      ],
      witnessData: [
        { id: '1', name: '@kutygee' },
        { id: '2', name: '@thegenius' },
        { id: '3', name: '@kutygee' },
        { id: '4', name: '@thegenius' },
        { id: '5', name: '@kutygee' },
        { id: '6', name: '@thegenius' },
        { id: '7', name: '@kutygee' },
        { id: '8', name: '@thegenius' },
        { id: '9', name: '@kutygee' },
        { id: '10', name: '@darkspot' }
      ]
    })
  }
</script>

<style>
  /* Create two unequal columns that floats next to each other */
  .mainColumn { float: left; width: 65%; padding: 1%; } 
  .rightColumn { float: left; width: 35%; padding: 1%; }

  /* Responsive layout - when the screen is less than 1200px wide, make the two leftmost columns stack side by side and on top of the third */
  @media screen and (max-width: 1200px) {
    /* Resize columns to fill page */
    .mainColumn, .rightColumn { width: 100%; padding: 0.5%; }
  }
</style>
