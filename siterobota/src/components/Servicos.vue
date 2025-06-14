<script setup>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import { ref } from 'vue'
const images = ref([
  { id: 1, src: "src/assets/test1.jpg", alt: 'Imagem 1' },
  { id: 2, src: "src/assets/test2.jpg", alt: 'Imagem 2' },
  { id: 3, src: "src/assets/test3.jpg", alt: 'Imagem 3' },
  { id: 4, src: "src/assets/test4.jpg", alt: 'Imagem 4' },
  { id: 5, src: "src/assets/test5.jpg", alt: 'Imagem 5' },
])
</script>

<template>
<div id="main-container">
    <h2>SERVIÇOS</h2>
    <div id="servicos">
        <div id="descricao">
            <h3>Também ofertamos os seguintes serviços para membros da graduação e empresas: </h3>
            <ul>
                <li>Impressão 3D</li>
                <li>Modelagem</li>
                <li>Mecânica</li>
                <li>Eletrônica</li>
            </ul>
        </div>
        <div id="carrossel">
            <Carousel :items-to-show="1" :wrap-around="true">
                <Slide v-for="image in images" :key="image.id">
                    <div class="carousel__item">
                        <img :src="image.src" :alt="image.alt" />
                    </div>
                </Slide>

                <template #addons>
                    <Navigation />
                    <Pagination />
                </template>
            </Carousel>
        </div>
    </div>
    
    
</div>

</template>

<style scoped>
    #main-container {
        @media screen and (max-width: 1200px) {
            margin-left: 96px;
            margin-right: 96px;
        }
        margin-left: 256px;
        margin-right: 256px;
        #servicos {
            display: flex;
            gap: 64px;
        }
        #descricao {
            h3 {
                font-size: 24px;
                line-clamp: 3;
            }
            li {
                font-size: 24px;
            }
        }
        #carrossel {
            width: 100%;
        }
        .carousel__item {
            width: 100%;
            overflow: hidden;
            img {
                border-radius: 16px;
                width: 100%;
                height: 100%;
                max-height: 384px;
                object-fit: cover;
            }
        }
        
    }
    .carousel__pagination {
        --vc-pgn-background-color: rgba(255, 255, 255, 0.7);
        --vc-pgn-active-color: rgba(255, 255, 255, 1);
    }
</style>
<style>
    .carousel__prev,
    .carousel__next {
        box-sizing: content-box;
        background-color: aliceblue;
        width: 32px;
        height: 100%;
    }
</style>