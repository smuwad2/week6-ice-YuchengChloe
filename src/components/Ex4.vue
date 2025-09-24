<script>
    export default { 
        data() {
            return {
                // Add code here
                id: "demo1",
                blueButton: true
            }
        },
        methods: { 
   			// Add code here
            changeColor(){
                this.blueButton = !this.blueButton
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    

    <div class="container">
        <div v-bind:id="id" class="m-2" v-bind:class="{'blueBox': blueButton, 'redBox': !blueButton}">
            div ID : {{id}} 
        </div>
        
        <button type="button" v-bind:class="{'btn btn-primary': blueButton, 'btn btn-danger': !blueButton}"
        @click="changeColor()">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
