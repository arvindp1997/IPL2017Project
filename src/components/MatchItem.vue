<template>
    <div class="match-item">
        <p> Match No. {{match.id}}</p>
        <p> Location: {{match.city}}</p>
        <p>Played on {{match.date}}</p>
        <p> Venue : {{match.venue}}</p>
        <p> {{match.team1}} VS {{match.team2}}</p>
          
        <p> Toss won by {{match.toss_winner}} and chose to {{match.toss_decision}} first</p>
        <p> Match result: {{match.result}}</p>
        <p> Match was won by {{match.winner}} by {{match.win_by_runs}} runs and by {{match.win_by_wickets}} wickets</p>
        <p>Man of the match:{{match.player_of_match}}</p> 
        <p>Umpires on the field were : {{match.umpire1}}
            ,{{match.umpire2}}
           
        </p>
    </div>
</template>

<script>
export default {
    name:"MatchItem",
    props:["match"],
    method:{
        getTeamImage: function(teamName) {
            if(teamName === 'Sunrisers Hyderabad')
            return (
            <img alt="SRH LOGO" src="./assets/teams/SRH.png"/>
            );
        }
    }
}
</script>

<style scoped>

 .match-item{
background-color: #20bf55;
background-image: linear-gradient(315deg, #20bf55 0%, #01baef 74%);


 }
 

</style>