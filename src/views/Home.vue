<template>

    <div class="Home-body-color">
        <HeaderApp></HeaderApp>
        <div class="container mt-5">
            <div class="row">
                <div v-for="image in dataImage" :key="image.url" class="col-3 mx-4">
                    <ImageGallery 
                        :srcImage="image.url"
                        :titleImage="image.titleImage"  
                    >
                                
                    </ImageGallery>
                </div>
                <div v-for="image in dataImage" :key="image.titleImage" class="col-3 mx-4">
                    <ImageGallery 
                        :srcImage="image.url"
                        :titleImage="image.titleImage"  
                    >
                                
                    </ImageGallery>
                </div>
            </div>
        </div>
    </div>
    
</template>

<script>

import HeaderApp from '@/components/layouts/HeaderApp.vue'
import ImageGallery from '@/components/layouts/ImageGallery.vue'


export default {
     data(){
        return{
            dataImage : [
                { url : 'https://picsum.photos/300/200?image=244' , titleImage : 'Pelicanos'},
                { url : 'https://picsum.photos/300/200?image=1024' , titleImage : 'Pato Aguila'},
                { url : 'https://picsum.photos/300/200?image=611', titleImage : 'Pelicanos All' }     
            ]
        }
    },
    components: {
        HeaderApp,
        ImageGallery
    }
}

</script>

<style scoped>

.Home-body-color{
    background-color: #fdfdfd ; 
}
    
</style>