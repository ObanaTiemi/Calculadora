<template>
    <div class="calcular" align="left" id="calculaNum">
            <div>X: <input type="number" v-model="valorX" :class="this.errox"   placeholder="Valor de x"/>
                 Y: <input type="number" v-model="valorY" :class="this.erroy" placeholder="Valor de y"/>
                <button v-on:click="calculaMais()" class="btn btn-primary" id="mais">x+y</button>
                <button v-on:click="calculaMenos()" class="btn btn-primary" id="menos">x-y</button>
                <button v-on:click="calculaMulti()" class="btn btn-primary" id="vezes">x*y</button>
                <button v-on:click="calculaDivisao()" class="btn btn-primary" id="dividido">x/y</button>
            </div>
            <div>
                Resultado: <input type="text" v-model="this.result"/>
            </div>
    </div>
</template>

<script>
export default {
    name: 'Calcula',
    data(){
        return{
            errox: '',
            erroy: '',
            result: ''
        }
    },
    methods:{
        calculaMais: function(x,y){
                    x = parseInt(this.valorX);
                    y = parseInt(this.valorY);
                    if(x <= 0 || y <= 0 ){
                        alert("Insira um número maior que 0");
                        this.errox = "erro";
                        this.erroy = "erro";
                    }else if(!(isNaN(x)) && !(isNaN(y))){
                        this.result = x+y;
                    }   
                    else{
                        alert("Insira um número");
                        this.errox = "erro";
                        this.erroy = "erro";
                    }
                        },
        calculaMenos: function(x,y){
                    x = parseInt(this.valorX);
                    y = parseInt(this.valorY);
                    if(x <= 0 || y <= 0 ){
                        alert("Insira um número maior que 0");
                        this.errox = "erro";
                        this.erroy = "erro";
                    }else if(!(isNaN(x)) && !(isNaN(y))){
                        this.result = x-y;
                    }   
                    else{
                        alert("Insira um número");
                        this.errox = "erro";
                        this.erroy = "erro";
                    }
                },
        calculaMulti: function(x,y){
                    x = parseInt(this.valorX);
                    y = parseInt(this.valorY);
                    if(x <= 0 || y <= 0 ){
                        alert("Insira um número maior que 0");
                        this.errox = "erro";
                        this.erroy = "erro";
                    }else if(!(isNaN(x)) && !(isNaN(y))){
                        this.result = x*y;
                    }   
                    else{
                        alert("Insira um número");
                        this.errox = "erro";
                        this.erroy = "erro";
                    }
                 },
        calculaDivisao: function(x,y){
                    x = parseInt(this.valorX);
                    y = parseInt(this.valorY);
                    if(x <= 0 || y <= 0 ){
                        alert("Insira um número maior que 0");
                        this.errox = "erro";
                        this.erroy = "erro";
                    }else if(!(isNaN(x)) && !(isNaN(y))){
                        this.result = x/y;
                    }   
                    else{
                        alert("Insira um número");
                        this.errox = "erro";
                        this.erroy = "erro";
                    }
                 }
            },
    }
</script>

<style scoped>
    .erro{
        background-color: red;
    }
</style>

