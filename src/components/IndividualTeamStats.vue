<template>
    <div class ="team">
     <h1 class="subheading grey--text">Team Stats</h1>
     <v-container class="my-5">
             <v-layout row wrap >
                 <v-flex xs12 sm6 md4 lg3 v-for="team in teams" :key="team.name">
                      <v-card flat class="text-xs-centered ma-3">
                        <v-responsive class="pt-4" v-if="team.name=== 'Kings XI Punjab'">
                            <img alt="KXIP" src="../assets/teams/KXIP.svg" width="300" height="300">
                        </v-responsive>
                          <v-responsive class="pt-4" v-if="team.name=== 'Delhi Daredevils'">
                            <img alt="DD" src="../assets/teams/DD1.png">
                        </v-responsive>
                          <v-responsive class="pt-4" v-if="team.name=== 'Kolkata Knight Riders'">
                            <img alt="KKR" src="../assets/teams/KKR.png">
                        </v-responsive>
                          <v-responsive class="pt-4" v-if="team.name=== 'Mumbai Indians'">
                            <img alt="MI" src="../assets/teams/MI.webp">
                        </v-responsive>
                          <v-responsive class="pt-4" v-if="team.name=== 'Royal Challengers Bangalore'">
                            <img alt="RCB" src="../assets/teams/RCB.png">
                        </v-responsive>
                          <v-responsive class="pt-4" v-if="team.name=== 'Sunrises Hyderabad'">
                            <img alt="SRH" src="../assets/teams/SRH1.png"  width="300" height="300">
                        </v-responsive>
                          <v-responsive class="pt-4" v-if="team.name=== 'Gujarat Lions'">
                            <img alt="GL" src="../assets/teams/GL.png">
                        </v-responsive>
                          <v-responsive class="pt-4" v-if="team.name=== 'Rising Pune SuperGiants'">
                            <img alt="RPS" src="../assets/teams/RPS.png">
                        </v-responsive>
                        
                        <v-card-text>
                            <h1>{{team.name}}</h1>
                              <h2>Match Winning Percentage:{{(team.won/team.played).toFixed(2)*100}}% </h2>

                             <h3>Total Matches Played:{{team.played}}</h3>
                             <h3>Total Matches Won:{{team.won}}</h3>
                             <h3>Total Matches Lost:{{team.lost}}</h3>
                             <h3>Total Matches Drawn:{{team.draw}}</h3>
                        </v-card-text>
                      </v-card>
                       <br/>
                     </v-flex> 
                    
             </v-layout>
     </v-container>

    </div>
</template>


<script>
export default {
    data() {
        return {
            teams:[
                {name:'Kings XI Punjab' ,won:43,lost:30,draw: 7, played:80  },
                  {name:'Kolkata Knight Riders' ,won:55,lost:20,draw: 5, played:80 },
                    {name:'Mumbai Indians' ,won:47,lost:30,draw: 3, played:80 },
                      {name:'Royal Challengers Bangalore' ,won:60,lost:18,draw: 2, played:80 },
                        {name:'Sunrises Hyderabad' ,won:26,lost:50,draw: 4, played:80 },
                          {name:'Delhi Daredevils' ,won:33,lost:45,draw: 2, played:80 },
                            {name:'Gujarat Lions' ,won:10,lost:65,draw: 5, played:80 },
                              {name:'Rising Pune SuperGiants' ,won:17,lost:60,draw: 2, played:79 }

            ]
        }
    }
}
</script>


<style scoped>

 .team{
background-color: #f9c5d1;
background-image: linear-gradient(315deg, #f9c5d1 0%, #9795ef 74%);



 }
 

</style>