<template>

<div id="header" :style="colorBlock">
  <h1>
    The Great 
    <br>
    <span id="colorDisplay">{{rgbmsg}}</span>
    <br>
     Guessing Game
  </h1>
</div>

</template>

<script lang="js">

  export default  {
    name: 'src-components-game-top',
    props: ['rgbmsg', 'hasWinner'],
    mounted () {

    },
    data () {
      return {
      }
    },
    methods: {

    },
    computed: {
      colorBlock: function() {
        console.log('Computed..'+ this.hide);
        let back = (this.hasWinner) ? this.rgbmsg : 'steelblue';

        return {
          'backgroundColor': back,
          'display': (this.hide) ? 'none' : 'block'
        };
      }
    }
}


</script>

<style scoped lang="css">

#header {
  transition: all 0.3s;
	background: steelblue;
	text-transform: uppercase;
	text-align: center;
	margin: 0;
	color: white;
}

h1 {
	font-weight: normal;
	line-height: 1.1;
	padding: 20px 0;

}

#colorDisplay {
	font-size: 200%;
}

</style>
