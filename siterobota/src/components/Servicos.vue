<script setup>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import { ref } from 'vue'

const images = ref([
  { id: 1, src: "src/assets/test1.jpg", alt: 'Robô Seguidor de Linha', title: 'Seguidor de Linha', description: 'Sistema autônomo de navegação' },
  { id: 2, src: "src/assets/test2.jpg", alt: 'Robô de Combate', title: 'Robô de Combate', description: 'Design robusto para competições' },
  { id: 3, src: "src/assets/test3.jpg", alt: 'Protótipo 3D', title: 'Prototipagem', description: 'Modelagem e impressão 3D' },
  { id: 4, src: "src/assets/test4.jpg", alt: 'Sistema Eletrônico', title: 'Eletrônica Embarcada', description: 'Circuitos personalizados' },
  { id: 5, src: "src/assets/test5.jpg", alt: 'Projeto Mecânico', title: 'Engenharia Mecânica', description: 'Soluções mecânicas inovadoras' },
])

const currentSlide = ref(0)
const carouselRef = ref(null)

const goToSlide = (index) => {
  if (carouselRef.value && carouselRef.value.slideTo) {
    carouselRef.value.slideTo(index)
  }
  currentSlide.value = index
}

const updateCurrentSlide = (data) => {
  currentSlide.value = data.currentSlideIndex
}
</script>

<template>
    <div id="main-container-servicos">
        <div class="section-header">
            <h2>SERVIÇOS</h2>
            <div class="accent-line"></div>
            <p class="section-description">
                Oferecemos serviços especializados para graduação e empresas
            </p>
        </div>

        <div id="servicos">
            <div class="services-content">
                <div class="services-list">
                    <h3>Nossos Serviços</h3>
                    <div class="service-grid">
                        <div class="service-item">
                            <div class="service-icon">🖨️</div>
                            <h4>Impressão 3D</h4>
                            <p>Prototipagem rápida e peças personalizadas</p>
                        </div>
                        <div class="service-item">
                            <div class="service-icon">📐</div>
                            <h4>Modelagem</h4>
                            <p>Design e modelagem CAD profissional</p>
                        </div>
                        <div class="service-item">
                            <div class="service-icon">⚙️</div>
                            <h4>Mecânica</h4>
                            <p>Soluções mecânicas e montagem</p>
                        </div>
                        <div class="service-item">
                            <div class="service-icon">🔌</div>
                            <h4>Eletrônica</h4>
                            <p>Circuitos e sistemas embarcados</p>
                        </div>
                    </div>
                </div>
            </div>

            <div class="gallery-section">
                <h3>Galeria de Trabalhos</h3>
                <div id="carrossel">
                    <Carousel
                        ref="carouselRef"
                        :items-to-show="1"
                        :wrap-around="true"
                        :autoplay="5000"
                        :pause-autoplay-on-hover="true"
                        :transition="500"
                        @slide-start="updateCurrentSlide"
                    >
                        <Slide v-for="(image, index) in images" :key="image.id">
                            <div class="carousel__item">
                                <div class="image-container">
                                    <img :src="image.src" :alt="image.alt" />
                                    <div class="image-overlay">
                                        <div class="overlay-content">
                                            <h4>{{ image.title }}</h4>
                                            <p>{{ image.description }}</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </Slide>

                        <template #addons>
                            <Navigation />
                            <Pagination />
                        </template>
                    </Carousel>

                    <!-- Thumbnails -->
                    <div class="carousel-thumbnails">
                        <div
                            v-for="(image, index) in images"
                            :key="'thumb-' + image.id"
                            class="thumbnail-item"
                            :class="{ active: index === currentSlide }"
                            @click="goToSlide(index)"
                        >
                            <img :src="image.src" :alt="image.alt" />
                            <div class="thumbnail-overlay">
                                <span class="thumbnail-title">{{ image.title }}</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
#main-container-servicos {
    max-width: 1200px;
    margin: 0 auto;
    padding: 80px 20px;
}

.section-header {
    text-align: center;
    margin-bottom: 60px;

    h2 {
        font-size: 2.5rem;
        font-weight: 700;
        background: linear-gradient(135deg, var(--main-purple), var(--main-orange));
        -webkit-background-clip: text;
        background-clip: text;
        -webkit-text-fill-color: transparent;
        margin-bottom: 20px;
    }

    .accent-line {
        width: 80px;
        height: 4px;
        background: linear-gradient(90deg, var(--main-purple), var(--main-orange));
        margin: 0 auto 20px;
        border-radius: 2px;
    }

    .section-description {
        font-size: 1.1rem;
        color: #666;
        max-width: 600px;
        margin: 0 auto;
        line-height: 1.6;
    }
}

#servicos {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: start;
}

.services-content {
    .services-list {
        background: white;
        padding: 40px;
        border-radius: 20px;
        box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08);
        border: 1px solid rgba(102, 51, 153, 0.1);

        h3 {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--main-purple);
            margin: 0 0 30px 0;
            text-align: center;
        }

        .service-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;

            .service-item {
                text-align: center;
                padding: 25px 15px;
                border-radius: 15px;
                transition: all 0.3s ease;
                border: 1px solid rgba(102, 51, 153, 0.1);

                &:hover {
                    background: linear-gradient(135deg, rgba(102, 51, 153, 0.05), rgba(255, 153, 51, 0.05));
                    transform: translateY(-5px);
                    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
                }

                .service-icon {
                    font-size: 2.5rem;
                    margin-bottom: 15px;
                }

                h4 {
                    font-size: 1.2rem;
                    font-weight: 600;
                    color: var(--secondary-dark-purple);
                    margin: 0 0 10px 0;
                }

                p {
                    font-size: 0.9rem;
                    color: #666;
                    line-height: 1.5;
                    margin: 0;
                }
            }
        }
    }
}

.gallery-section {
    h3 {
        font-size: 1.8rem;
        font-weight: 700;
        color: var(--main-purple);
        margin: 0 0 30px 0;
        text-align: center;
    }

    #carrossel {
        background: white;
        border-radius: 20px;
        overflow: hidden;
        box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08);
        border: 1px solid rgba(102, 51, 153, 0.1);

        .carousel__item {
            width: 100%;
            height: 400px;
            overflow: hidden;
            position: relative;

            .image-container {
                width: 100%;
                height: 100%;
                position: relative;
                overflow: hidden;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                    transition: transform 0.3s ease;
                }

                .image-overlay {
                    position: absolute;
                    top: 0;
                    left: 0;
                    right: 0;
                    bottom: 0;
                    background: linear-gradient(
                        to bottom,
                        rgba(0, 0, 0, 0) 0%,
                        rgba(0, 0, 0, 0.4) 60%,
                        rgba(0, 0, 0, 0.8) 100%
                    );
                    display: flex;
                    align-items: flex-end;
                    opacity: 0;
                    transition: opacity 0.3s ease;

                    .overlay-content {
                        padding: 30px;
                        color: white;
                        width: 100%;
                        transform: translateY(20px);
                        transition: transform 0.3s ease;

                        h4 {
                            font-size: 1.5rem;
                            font-weight: 700;
                            margin: 0 0 10px 0;
                        }

                        p {
                            font-size: 1rem;
                            margin: 0 0 20px 0;
                            opacity: 0.9;
                        }

                        .view-details-btn {
                            background: linear-gradient(135deg, var(--main-purple), var(--main-orange));
                            color: white;
                            border: none;
                            padding: 12px 24px;
                            border-radius: 25px;
                            font-weight: 600;
                            cursor: pointer;
                            transition: all 0.3s ease;
                            font-size: 0.9rem;

                            &:hover {
                                transform: translateY(-2px);
                                box-shadow: 0 8px 20px rgba(102, 51, 153, 0.3);
                            }
                        }
                    }
                }

                &:hover {
                    .image-overlay {
                        opacity: 1;

                        .overlay-content {
                            transform: translateY(0);
                        }
                    }

                    img {
                        transform: scale(1.05);
                    }
                }
            }
        }
    }

    .carousel-thumbnails {
        display: flex;
        justify-content: center;
        gap: 12px;
        padding: 20px;
        background: rgba(248, 250, 252, 0.9);
        margin-top: -1px;

        .thumbnail-item {
            width: 60px;
            height: 40px;
            border-radius: 8px;
            overflow: hidden;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
            position: relative;

            &.active {
                border-color: var(--main-purple);
                transform: scale(1.1);
            }

            &:hover {
                transform: scale(1.05);
            }

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }

            .thumbnail-overlay {
                position: absolute;
                bottom: 0;
                left: 0;
                right: 0;
                background: linear-gradient(transparent, rgba(0, 0, 0, 0.8));
                color: white;
                padding: 4px;
                opacity: 0;
                transition: opacity 0.3s ease;

                .thumbnail-title {
                    font-size: 0.7rem;
                    font-weight: 600;
                    display: block;
                    text-align: center;
                    white-space: nowrap;
                    overflow: hidden;
                    text-overflow: ellipsis;
                }
            }

            &:hover .thumbnail-overlay {
                opacity: 1;
            }
        }
    }
}

@media screen and (max-width: 1200px) {
    #main-container-servicos {
        padding: 60px 30px;
    }

    #servicos {
        gap: 30px;
    }
}

@media screen and (max-width: 768px) {
    #main-container-servicos {
        padding: 50px 20px;
    }

    .section-header h2 {
        font-size: 2rem;
    }

    .section-header .section-description {
        font-size: 1rem;
    }

    #servicos {
        grid-template-columns: 1fr;
        gap: 30px;
    }

    .services-list {
        padding: 30px 25px !important;

        h3 {
            font-size: 1.8rem;
        }

        .service-grid {
            grid-template-columns: repeat(2, 1fr) !important;
            gap: 20px !important;
        }

        .service-item {
            padding: 20px 15px;

            .service-icon {
                font-size: 2rem;
            }

            h4 {
                font-size: 1.1rem;
            }

            p {
                font-size: 0.9rem;
            }
        }
    }

    .gallery-section {
        h3 {
            font-size: 1.8rem;
        }
    }

    .carousel__item {
        height: 280px !important;
    }

    .carousel-thumbnails {
        grid-template-columns: repeat(3, 1fr) !important;
        gap: 10px !important;

        .thumbnail-item {
            height: 60px !important;
        }
    }
}

@media screen and (max-width: 480px) {
    #main-container-servicos {
        padding: 40px 15px;
    }

    .section-header h2 {
        font-size: 1.8rem;
    }

    .services-list {
        padding: 25px 20px !important;

        h3 {
            font-size: 1.6rem;
        }

        .service-grid {
            grid-template-columns: 1fr !important;
            gap: 15px !important;
        }

        .service-item {
            padding: 18px 15px;

            .service-icon {
                font-size: 1.8rem;
            }

            h4 {
                font-size: 1rem;
            }

            p {
                font-size: 0.85rem;
            }
        }
    }

    .gallery-section {
        h3 {
            font-size: 1.6rem;
        }
    }

    .carousel__item {
        height: 250px !important;
    }

    .carousel-thumbnails {
        display: none !important;
    }

    .overlay-content {
        padding: 15px;

        h4 {
            font-size: 1.2rem;
        }

        p {
            font-size: 0.9rem;
        }

        .view-details-btn {
            padding: 8px 16px;
            font-size: 0.85rem;
        }
    }
}

@media screen and (max-width: 360px) {
    .section-header h2 {
        font-size: 1.6rem;
    }

    .carousel__item {
        height: 220px !important;
    }
}
</style>

<style>
/* Estilos personalizados para o carrossel */
.carousel__pagination {
    padding: 15px 0;
    margin: 0;
    background: rgba(248, 250, 252, 0.9);
}

.carousel__pagination-button {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: rgba(102, 51, 153, 0.3);
    border: none;
    margin: 0 6px;
    transition: all 0.3s ease;
    cursor: pointer;
}

.carousel__pagination-button--active {
    background-color: var(--main-purple);
    transform: scale(1.2);
}

.carousel__pagination-button:hover {
    background-color: var(--main-purple);
    transform: scale(1.1);
}

.carousel__prev,
.carousel__next {
    width: 45px;
    height: 45px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--main-purple), var(--main-orange));
    border: none;
    color: white;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(102, 51, 153, 0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 10px;
}

.carousel__prev:hover,
.carousel__next:hover {
    transform: scale(1.1);
    box-shadow: 0 6px 20px rgba(102, 51, 153, 0.4);
}

/* Ícones das setas */
.carousel__prev::before {
    content: '‹';
    font-size: 20px;
}

.carousel__next::before {
    content: '›';
    font-size: 20px;
}

/* Ocultar os ícones padrão */
.carousel__icon {
    display: none;
}
</style>