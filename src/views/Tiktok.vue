<template>
    <div class="container">
        <h1>Total Like = {{ totalLike }}</h1>
        <h1>Total Love = {{ totalLove }}</h1>
        <tt v-for="(item, index) in tiktokData" 
        :key="index" 
        :image="item.image" 
        :title="item.title" 
        :tag="item.tag"
        @callbackLike="likel"
        @callbackLove="lovel"
        />
    </div>
</template>

<script>
import tt from "@/components/Tiktok.vue";

export default {
    components: {
        tt
    },
    
    data() {
        return {
            tiktokData:[
                {image:'https://s.isanook.com/ga/0/rp/r/w728/ya0xa0m1w0/aHR0cHM6Ly9zLmlzYW5vb2suY29tL2dhLzAvdWQvMjE0LzEwNzI2NDkvcm92LSgxKS5qcGc=.jpg',title:'rov',tag:'#rov'},
                {image:'https://scontent.fbkk10-1.fna.fbcdn.net/v/t1.0-9/148002871_1946937168803056_3665339096045154358_o.png?_nc_cat=108&ccb=3&_nc_sid=dbeb18&_nc_eui2=AeGnld2SzDDKM2LJCyjrQ-KiLhZX_GN-Mr8uFlf8Y34yv3gc0qVUN0qOZvNcFSA1wkyr5byFITMqzyefZ2xGPJ1W&_nc_ohc=3o9hftcJTVIAX9LUfaH&_nc_ht=scontent.fbkk10-1.fna&oh=e6780bccda22fb48005d2def58401619&oe=604AE6A4',title:'alice',tag:'#alice'},
                {image:'',title:'',tag:''},
                {image:'',title:'',tag:''},
                {image:'',title:'',tag:''}
            ],
            totalLike:0,
            totalLove:0
        };
    },
    methods:{
        likel(){
            this.totalLike ++;
        },
        lovel(){
            this.totalLove ++;
        }
        
    }
};
</script>

<style>

</style>