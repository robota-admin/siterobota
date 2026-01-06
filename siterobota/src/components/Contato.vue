<script setup>
</script>

<template>
    <div id="main-container-contato">
        <div class="section-header">
            <h2>CONTATO</h2>
            <div class="accent-line"></div>
            <p class="section-description">
                Entre em contato conosco para parcerias, dúvidas ou participar da equipe
            </p>
        </div>

        <div class="contact-content">
            <div class="contact-info">
                <div class="info-card">
                    <div class="info-header">
                        <div class="info-icon">🏢</div>
                        <h3>ROBOTA UFSC</h3>
                    </div>

                    <div class="info-item">
                        <div class="item-icon">📍</div>
                        <div class="item-content">
                            <h4>Localização</h4>
                            <p>LTIC - Laboratório de Tecnologia e Comunicação<br>
                               Av. Prof. Henrique da Silva Fontes, 1 - Trindade<br>
                               Florianópolis - SC, 88036-700</p>
                        </div>
                    </div>

                    <div class="info-item">
                        <div class="item-icon">📧</div>
                        <div class="item-content">
                            <h4>Email</h4>
                            <p>robotadasufsc@gmail.com</p>
                        </div>
                    </div>

                    <div class="info-item">
                        <div class="item-icon">📱</div>
                        <div class="item-content">
                            <h4>WhatsApp</h4>
                            <p>(48) 3721-4609</p>
                        </div>
                    </div>

                    <div class="social-section">
                        <h4>Redes Sociais</h4>
                        <div class="social-links">
                            <a href="https://www.instagram.com/robota.ufsc/" class="social-link" title="Instagram" target="_blank" rel="noopener noreferrer">
                                <img src="../assets/icons8-instagram.svg" alt="Instagram">
                            </a>
                            <a href="#" class="social-link" title="Facebook">
                                <img src="../assets/icons8-facebook.svg" alt="Facebook">
                            </a>
                            <a href="#" class="social-link" title="TikTok">
                                <img src="../assets/icons8-tiktok.svg" alt="TikTok">
                            </a>
                            <a href="#" class="social-link" title="Twitter">
                                <img src="../assets/icons8-twitter.svg" alt="Twitter">
                            </a>
                        </div>
                    </div>
                </div>
            </div>

            <div class="map-section">
                <div class="map-container">
                    <div class="map-placeholder">
                        <img src="../assets/mapstest.png" alt="Localização da ROBOTA">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
#main-container-contato {
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

.contact-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: start;
}

.contact-info {
    .info-card {
        background: white;
        padding: 40px;
        border-radius: 20px;
        box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08);
        border: 1px solid rgba(102, 51, 153, 0.1);

        .info-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid rgba(102, 51, 153, 0.1);

            .info-icon {
                font-size: 2.5rem;
            }

            h3 {
                font-size: 1.8rem;
                font-weight: 700;
                color: var(--main-purple);
                margin: 0;
            }
        }

        .info-item {
            display: flex;
            gap: 15px;
            margin-bottom: 25px;

            .item-icon {
                font-size: 1.5rem;
                margin-top: 5px;
                flex-shrink: 0;
            }

            .item-content {
                h4 {
                    font-size: 1.1rem;
                    font-weight: 600;
                    color: var(--secondary-dark-purple);
                    margin: 0 0 8px 0;
                }

                p {
                    font-size: 1rem;
                    color: #666;
                    line-height: 1.6;
                    margin: 0;
                }
            }
        }

        .social-section {
            margin-top: 30px;
            padding-top: 25px;
            border-top: 1px solid rgba(102, 51, 153, 0.1);

            h4 {
                font-size: 1.1rem;
                font-weight: 600;
                color: var(--secondary-dark-purple);
                margin: 0 0 15px 0;
            }

            .social-links {
                display: flex;
                gap: 12px;

                .social-link {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    width: 45px;
                    height: 45px;
                    background: rgba(102, 51, 153, 0.1);
                    border-radius: 50%;
                    transition: all 0.3s ease;

                    img {
                        width: 22px;
                        height: 22px;
                        opacity: 0.7;
                        transition: all 0.3s ease;
                    }

                    &:hover {
                        background: linear-gradient(135deg, var(--main-purple), var(--main-orange));
                        transform: translateY(-3px);
                        box-shadow: 0 8px 20px rgba(102, 51, 153, 0.3);

                        img {
                            opacity: 1;
                            filter: brightness(0) invert(1);
                        }
                    }
                }
            }
        }
    }
}

.map-section {
    .map-container {
        background: white;
        border-radius: 20px;
        overflow: hidden;
        box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08);
        border: 1px solid rgba(102, 51, 153, 0.1);

        .map-placeholder {
            width: 100%;
            height: 400px;
            position: relative;
            overflow: hidden;

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                transition: transform 0.3s ease;
            }

            &:hover img {
                transform: scale(1.05);
            }
        }
    }
}

@media screen and (max-width: 1200px) {
    #main-container-contato {
        padding: 60px 30px;
    }
}

@media screen and (max-width: 768px) {
    #main-container-contato {
        padding: 50px 20px;
    }

    .section-header h2 {
        font-size: 2rem;
    }

    .section-header .section-description {
        font-size: 1rem;
    }

    .contact-content {
        grid-template-columns: 1fr;
        gap: 30px;
    }

    .info-card {
        padding: 30px 25px !important;

        .info-header {
            margin-bottom: 25px !important;

            .info-icon {
                font-size: 2rem !important;
            }

            h3 {
                font-size: 1.5rem !important;
            }
        }

        .info-item {
            margin-bottom: 20px;

            .item-content h4 {
                font-size: 1.1rem;
            }

            .item-content p {
                font-size: 0.95rem;
            }
        }

        .social-section h4 {
            text-align: center;
            font-size: 1.1rem;
        }
    }

    .map-placeholder {
        height: 300px !important;
    }
}

@media screen and (max-width: 480px) {
    #main-container-contato {
        padding: 40px 15px;
    }

    .section-header h2 {
        font-size: 1.8rem;
    }

    .info-card {
        padding: 25px 20px !important;

        .info-header {
            h3 {
                font-size: 1.3rem !important;
            }
        }
    }

    .info-item {
        flex-direction: column;
        gap: 8px !important;
        text-align: center;

        .item-icon {
            align-self: center;
            margin-top: 0 !important;
        }

        .item-content {
            h4 {
                font-size: 1rem;
            }

            p {
                font-size: 0.9rem;
            }
        }
    }

    .social-links {
        justify-content: center;
        gap: 12px;

        .social-link {
            width: 45px;
            height: 45px;

            img {
                width: 22px;
                height: 22px;
            }
        }
    }

    .map-placeholder {
        height: 250px !important;
    }
}

@media screen and (max-width: 360px) {
    .section-header h2 {
        font-size: 1.6rem;
    }

    .info-item .item-content p {
        font-size: 0.85rem;
    }

    .map-placeholder {
        height: 220px !important;
    }
}
</style>