<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="changeComponent = 'appBlue'">Load Blue Template</button>
                <button class="btn btn-success" @click="changeComponent = 'appGreen'">Load Green Template</button>
                <button class="btn btn-danger" @click="changeComponent = 'appRed'">Load Red Template</button>
                <hr>
                <!-- <app-blue>
                  <h1 slot="blue">blue</h1>
                </app-blue>
                <app-green>
                  <h1 slot="green">green</h1>
                </app-green>
                <app-red>
                  <h1 slot="red">red</h1>
                </app-red> -->
                <component :is="changeComponent"></component>
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
      data(){
        return{
          changeComponent : 'appBlue'
        }
      },
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        }
    }
</script>

<style>
</style>
