<template>
    <div>
        <ul id="todo-items" >
            <li v-for="(item, index) in todolist" v-bind:key="index">
                {{index}} {{item.name}} {{item.done}}

            </li>
        </ul> 
        <input id="todo-list-item" type="text" placeholder="Enter Todo"
                v-model="item">
        <button type="submit" v-on:click="submitItem(item)">
            Lägg till Todo
        </button>
    </div>
</template>

<script>

export default { 
name:"listitems",

    data(){
            return{
                item:'',
                todolist:[]
            }
        },

    props:{
        name:String,
        done:Boolean,
        
    },
        methods:{
        submitItem(item){
            this.$emit
            //{if (this.item.length > 0 ) }  
            {this.todolist.push({name:item, done:false}) }
            {this.item = ''}
            console.log(`the method in listitem ${item}`);
               
    }  }

}
</script>

<style scoped>
ul { list-style-type:none;}
</style>