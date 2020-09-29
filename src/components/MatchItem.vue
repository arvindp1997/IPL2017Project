<template>
    <div class="match-item">
        <h1> Match No. {{match.id}}</h1>
        <h2> Location: {{match.city}}</h2>
        <h3>Played on {{match.date}}</h3>
        <h3> Venue : {{match.venue}}</h3>
        <h3> {{match.team1}} VS {{match.team2}}</h3>
          
        <h3> Toss won by {{match.toss_winner}} and chose to {{match.toss_decision}} first</h3>
        <h3> Match result: {{match.result}}</h3>
        <h3> Match was won by {{match.winner}} by {{match.win_by_runs}} runs and by {{match.win_by_wickets}} wickets</h3>
        <h3>Man of the match:{{match.player_of_match}}</h3> 
        <h3>Umpires on the field were : {{match.umpire1}}
            ,{{match.umpire2}}
           
        </h3>
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
background-color: #cfc7f8;
background-image: linear-gradient(315deg, #cfc7f8 0%, #ebbba7 74%);


 }
 

</style>