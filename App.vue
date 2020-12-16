<template>


    <div class=" boxshadow configbox">

        <header class="center">
            <h1  style="text-align: center;">TEFLON</h1>
            <img src="./images/microwave-24px.svg" alt="img" style="text-align: center;">
            <h6  style="text-align: center;">När det inte fastnar</h6> 
            <!--<p id="counter" style="text-align: center;" class="flex-row"></p> -->
        </header>

        
            <!--3.använda listitems. placeholder for Todo items -->
        <listitems />
           
               
        
    </div>

</template>

<script>
import listitems from './listitems.vue' //1.App.vue har nu tillgång till listitems component. listitems här är en variabel .


export default {
name:"app",
    
        //2.Vi registrera listitems här nyckel:värdet(det du vill importera) 
     
    data(){},
    
    components:{listitems: listitems}
                   

}
</script>

<style scoped>

.configbox{
    background-color: palevioletred;
    align-items: center;
    justify-content: center;
    width: 25%;
}


.boxshadow
{
-webkit-box-shadow: 0px 0px 20px -5px rgba(0,0,0,0.57);
-moz-box-shadow: 0px 0px 20px -5px rgba(0,0,0,0.57);
box-shadow: 0px 0px 20px -5px rgba(0,0,0,0.57);
}

.center{justify-content: center;
        align-items: center;}
</style>