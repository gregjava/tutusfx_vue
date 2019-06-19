<template>
  <v-app id="app">
    <v-container fluid class="row">
      <v-layout leftColumn>
        <v-flex class="card">
          <v-card class="segment"><br/>
            <h3>Top Trades</h3><hr><br>
            <span
              v-for="item in Trades"
              :key="item.id"
            >
              <div class="imgholder trendingtrades">
                <p class="trendingtradeusername">
                  {{ item.currency }};
                </p>
                <p>Current Profit: {{ item.profit }}; Profit Margin: {{ item.margin }};</p>
                <p>Trade Volume: {{ item.volume }}; Token Charges: {{ item.charge }};</p>
                <p><a href="../@item.namehash">{{ item.namehash }};</a></p>
              </div><hr><br></span>
          </v-card>
          <v-card class="segment"><br/>
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
          <v-card class="segment"><br/>
            <h3>About Tutusfx</h3><hr>
            <img 
              class="imgholder picture" 
              src="../assets/images/logo_bar.png" 
              width="100%" 
              height="100%" 
              alt="Tutusfx logo"
            >
            <p>The threshold to create and operate a Marketing Network is quite high! Therefore, a one-stop solution is provided by the Tutusfx Community for anyone to create a unique Network without any thresholds.</p>
            <p 
              class="rightAlign"
            >
              <router-link to="/about">More...</router-link>
            </p><br><br><hr><br>
          </v-card>
        </v-flex>
      </v-layout>
      <v-layout mainColumn>
        <v-flex class="card">
          <v-card class="tradeview animatePix segment">
            <span class="header"> <h1 class="headertitle"> Tutusfx </h1> <span class="headercontent"> An incentivized trade network built on blockchain technology </span> </span>
          </v-card>
          <v-card class="segment">
            <br>
            <h3>Trending Posts</h3><hr>
            <span
              v-for="item in TrendingPosts" 
              :key="item.id" 
            ><br>
              <h5><b> {{ item.desc }}</b></h5><br/><h6 class="rightAlign">{{ item.date }}</h6>
              <div class="imgholder largepicture">
                {{ item.img }}
              </div><hr>
              <p>{{ item.txt1 }}</p>
              <p>{{ item.txt2 }}</p><hr><br>
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
          >
            <br>
            <h3>{{ item.title }}</h3><hr>
            <h5><b> {{ item.desc }}</b></h5><br/><h6 class="rightAlign">{{ item.date }}</h6>
            <div class="imgholder largepicture">
              {{ item.img }}
            </div><hr>
            <p>{{ item.txt1 }}</p>
            <p>{{ item.txt2 }}</p><hr><br>
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
      TrendingPosts: [
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
        }
      ],
      AllPosts: [
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
          title: 'Blockchain Post 3',
          desc: 'Title description',
          date: 'Dec 10, 2018',
          img: 'Image',
          txt1: 'Some text from Post 3...',
          txt2: 'Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.',
          views: '258',
          interactions: '14',
          comments: '5'
        }
      ],
      Trades: [
        {
          currency: 'USD/AUD',
          profit: '+$309.82',
          margin: '+31.01',
          volume: '$10.00',
          charge: '$2.8',
          namehash: 'guest#609325cwq98'
        },
        {
          currency: 'USD/GBP',
          profit: '+$287.10',
          margin: '+42.35',
          volume: '$7.00',
          charge: '$9.35',
          namehash: 'guest#302q25%eo4j'
        },
        {
          currency: 'USD/CAD',
          profit: '+$684.37',
          margin: '+13.70',
          volume: '$50.00',
          charge: '$0.63',
          namehash: 'guest#48557310~u2'
        }
      ], drawer: false,
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
</style>
