<script setup>
</script>

<template>
    <div id="main-container-equipes">
        <div class="section-header">
            <h2>NOSSAS EQUIPES</h2>
            <div class="accent-line"></div>
            <p class="section-description">
                Conheça as diferentes modalidades desenvolvidas pela ROBOTA
            </p>
        </div>

        <div id="equipes">
            <div class="equipe-card" id="trekking">
                <div class="card-header">
                    <div class="icon-wrapper trekking">
                        <span class="icon">🏔️</span>
                    </div>
                    <h3>Trekking</h3>
                </div>
                <div class="card-image">
                    <img src="../assets/trekking.JPG" alt="Robô Trekking">
                </div>
                <div class="card-content">
                    <p>
                        Robô móvel adaptado para situações de Off-road e On-road, capaz de realizar
                        um circuito desconhecido e com obstáculos de maneira completamente autônoma.
                        Combina princípios de mecânica, eletrônica, programação e modelagem 3D.
                    </p>
                    <div class="card-tags">
                        <span class="tag">Autonomia</span>
                        <span class="tag">Navegação</span>
                        <span class="tag">Obstáculos</span>
                    </div>
                </div>
            </div>

            <div class="equipe-card" id="combate">
                <div class="card-header">
                    <div class="icon-wrapper combate">
                        <span class="icon">⚔️</span>
                    </div>
                    <h3>Combate</h3>
                </div>
                <div class="card-image">
                    <img src="../assets/combate.JPG" alt="Robô Combate">
                </div>
                <div class="card-content">
                    <p>
                        Principal categoria em competições de robótica. Os robôs são separados por peso
                        e controlados por infravermelho. Focam em resistência, estratégia e mecanismos
                        de ataque e defesa. Combina princípios de mecânica, eletrônica e modelagem 3D.
                    </p>
                    <div class="card-tags">
                        <span class="tag">Estratégia</span>
                        <span class="tag">Resistência</span>
                        <span class="tag">Controle</span>
                    </div>
                </div>
            </div>

            <div class="equipe-card" id="seguidor">
                <div class="card-header">
                    <div class="icon-wrapper seguidor">
                        <span class="icon">🛤️</span>
                    </div>
                    <h3>Seguidor de Linha</h3>
                </div>
                <div class="card-image">
                    <img src="../assets/segue_linha.JPG" alt="Robô Seguidor de Linha">
                </div>
                <div class="card-content">
                    <p>
                        Robô autônomo projetado para seguir trajetórias pré-definidas com precisão e
                        velocidade, utilizando sensores ópticos e algoritmos de controle para manter
                        o percurso ideal em linhas brancas ou pretas.
                    </p>
                    <div class="card-tags">
                        <span class="tag">Precisão</span>
                        <span class="tag">Velocidade</span>
                        <span class="tag">Sensores</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
#main-container-equipes {
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

#equipes {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 30px;
    margin-top: 40px;
}

.equipe-card {
    background: white;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    transition: all 0.4s ease;
    overflow: hidden;
    border: 1px solid rgba(102, 51, 153, 0.1);

    &:hover {
        transform: translateY(-10px);
        box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
    }
}

.card-header {
    padding: 30px 30px 20px;
    text-align: center;

    .icon-wrapper {
        width: 70px;
        height: 70px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 0 auto 20px;

        .icon {
            font-size: 30px;
        }

        &.trekking {
            background: linear-gradient(135deg, var(--main-purple), var(--secondary-light-purple));
        }

        &.combate {
            background: linear-gradient(135deg, var(--main-orange), var(--secondary-light-orange));
        }

        &.seguidor {
            background: linear-gradient(135deg, var(--main-yellow), var(--secondary-light-yellow));
        }
    }

    h3 {
        font-size: 1.5rem;
        font-weight: 700;
        color: var(--secondary-dark-purple);
        margin: 0;
    }
}

.card-image {
    width: 100%;
    height: 200px;
    overflow: hidden;
    position: relative;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: transform 0.4s ease;
    }

    &:hover img {
        transform: scale(1.05);
    }
}

.card-content {
    padding: 30px;

    p {
        font-size: 0.95rem;
        line-height: 1.7;
        color: #555;
        margin-bottom: 25px;
    }

    .card-tags {
        display: flex;
        gap: 10px;
        flex-wrap: wrap;

        .tag {
            background: linear-gradient(135deg, var(--main-purple), var(--secondary-light-purple));
            color: white;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            opacity: 0.9;
        }
    }
}

@media screen and (max-width: 1200px) {
    #main-container-equipes {
        padding: 60px 30px;
    }

    #equipes {
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 25px;
    }
}

@media screen and (max-width: 768px) {
    #main-container-equipes {
        padding: 50px 20px;
    }

    .section-header h2 {
        font-size: 2rem;
    }

    .section-header .section-description {
        font-size: 1rem;
    }

    #equipes {
        grid-template-columns: 1fr;
        gap: 25px;
    }

    .card-header {
        padding: 25px 25px 15px;

        .icon-wrapper {
            width: 60px;
            height: 60px;

            .icon {
                font-size: 25px;
            }
        }

        h3 {
            font-size: 1.3rem;
        }
    }

    .card-content {
        padding: 25px;

        p {
            font-size: 0.9rem;
        }

        .card-tags .tag {
            font-size: 0.75rem;
            padding: 5px 12px;
        }
    }
}

@media screen and (max-width: 480px) {
    #main-container-equipes {
        padding: 40px 15px;
    }

    .section-header h2 {
        font-size: 1.8rem;
    }

    .card-header {
        padding: 20px 20px 15px;

        .icon-wrapper {
            width: 55px;
            height: 55px;
            margin-bottom: 15px;

            .icon {
                font-size: 22px;
            }
        }

        h3 {
            font-size: 1.2rem;
        }
    }

    .card-content {
        padding: 20px;

        p {
            font-size: 0.85rem;
            margin-bottom: 20px;
        }

        .card-tags {
            gap: 8px;

            .tag {
                font-size: 0.7rem;
                padding: 4px 10px;
            }
        }
    }

    .card-image {
        height: 180px;
    }
}

@media screen and (max-width: 360px) {
    .section-header h2 {
        font-size: 1.6rem;
    }

    .card-header h3 {
        font-size: 1.1rem;
    }

    .card-image {
        height: 160px;
    }
}
</style>
