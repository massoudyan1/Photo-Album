<template>
  <h1>PicList Works</h1>
  <div id="container">
  <div style="all:unset"  v-for="pic in this.pics" :key="pic">
  </div>
  </div>
</template>

<script>
import SinglePic from './SinglePic'

export default {
    name: 'Pic List',
    components: { SinglePic },
    data() {
        return {
            pics: []
        }
    },
    mounted() {
        fetch('http://localhost:3000/pics')
            .then(res => res.json())
            .then(data => this.pics = data)
            .catch(err => console.log(err.message))
        
    }
}
</script>

<style>
body {
    background-color: rgb(40, 40, 40);
}
#container {
    
    margin: 0 auto;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    box-sizing: border-box;
    align-content: space-around;
}

#container div * {
    box-sizing: border-box;
}

#container div .cell {
    width: 128px;
    height: 128px;
    padding: 2px;
    padding-bottom: 0;
    padding-top: 0;
}

#container div #clicked {
    padding: 1;
    border-bottom-right-radius: 20%;
    border-bottom: 1px solid white;
    border-top-left-radius: 20%;
    border-top: 2px solid white;
}

#container div #showing {
    width: 78vw;
    align-self: stretch;
    height: inherit;
    border-radius: 5px;
    margin: 3 0 3 0;
}

#container div .cell:hover, #container div #showing:hover {
    cursor: pointer;
}
@media ( max-width: 2304px ) {
    #container {
    width: 2048px;
    }
    #container div #showing {
    width: 2048px;
    }
}
@media ( max-width: 2176px ) {
    #container {
    width: 1920px;
    }
    #container div #showing {
    width: 1920px;
    }
}
@media ( max-width: 2048px ) {
    #container {
    width: 1792px;
    }
    #container div #showing {
    width: 1792px;
    }
}
@media ( max-width: 1920px ) {
    #container {
    width: 1664px;
    }
    #container div #showing {
    width: 1664px;
    }
}
@media ( max-width: 1792px ) {
    #container {
    width: 1536px;
    }
    #container div #showing {
    width: 1536px;
    }
}
@media ( max-width: 1664px ) {
    #container {
    width: 1408px;
    }
    #container div #showing {
    width: 1408px;
    }
}
@media ( max-width: 1536px ) {
    #container {
    width: 1280px;
    }
    #container div #showing {
    width: 1280px;
    }
}
@media ( max-width: 1408px ) {
    #container {
    width: 1152px;
    }
    #container div #showing {
    width: 1152px;
    }
}
@media ( max-width: 1280px ) {
    #container {
    width: 1024px;
    }
    #container div #showing {
    width: 1024px;
    }
}
@media ( max-width: 1152px ) {
    #container {
    width: 896px;
    }
    #container div #showing {
    width: 896px;
    }
}
@media ( max-width: 1024px ) {
    #container {
    width: 768px;
    }
    #container div #showing {
    width: 768px;
    }
}
@media ( max-width: 896px ) {
    #container {
    width: 640px;
    }
    #container div #showing {
    width: 640px;
    }
}
@media ( max-width: 768px ) {
    #container {
    width: 512px;
    }
    #container div #showing {
    width: 512px;
    }
}
@media ( max-width: 640px ) {
    #container {
    width: 384px;
    }
    #container div #showing {
    width: 384px;
    }
}
@media ( max-width: 512px ) {
    #container {
    width: 256px;
    }
    #container div #showing {
    width: 256px;
    }
}
</style>