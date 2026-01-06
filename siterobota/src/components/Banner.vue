<script setup>
</script>

<template>
    <div id="main-container">
        <div id="banner" style="background: url('public/banner_robota.JPG') no-repeat center center / cover;">
            <div class="banner-overlay"></div>
            <div id="heading-container">
                <div id="text-container">
                    <h1 class="main-title">EQUIPE DE COMPETIÇÃO DE ROBÓTICA MÓVEL</h1>
                    <h2 class="subtitle">CTC/DAS/UFSC</h2>
                    <p class="description">Inovação, tecnologia e conhecimento aplicados à robótica competitiva</p>
                </div>
                <div id="button-containers">
                    <button class="btn-primary">
                        <span><a href="https://linktr.ee/robotaufsc">PARTICIPAR</a></span>
                    </button>
                    <button class="btn-secondary">
                        <span><a href="#">APOIAR</a></span>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
#main-container {
    width: 100%;
    position: relative;
}

#banner {
    height: 70vh;
    min-height: 600px;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
}

.banner-overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(135deg, rgba(102, 51, 153, 0.8), rgba(255, 153, 51, 0.6));
    z-index: 1;
}

#heading-container {
    position: relative;
    z-index: 2;
    text-align: center;
    max-width: 800px;
    padding: 0 20px;
    animation: fadeInUp 1s ease-out;
}

#text-container {
    margin-bottom: 40px;
}

.main-title {
    color: white;
    font-size: 3.5rem;
    font-weight: 800;
    line-height: 1.1;
    margin-bottom: 20px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
    letter-spacing: -0.02em;
}

.subtitle {
    color: var(--secondary-light-yellow);
    font-size: 2rem;
    font-weight: 600;
    margin-bottom: 15px;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
}

.description {
    color: rgba(255, 255, 255, 0.9);
    font-size: 1.3rem;
    font-weight: 400;
    line-height: 1.6;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
    margin: 0;
}

#button-containers {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
}

.btn-primary,
.btn-secondary {
    padding: 16px 32px;
    font-size: 1.1rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1px;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
}

.btn-primary {
    background: linear-gradient(135deg, var(--main-purple), var(--secondary-light-purple));
    color: white;
    box-shadow: 0 8px 25px rgba(102, 51, 153, 0.4);
}

.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 12px 35px rgba(102, 51, 153, 0.5);
}

.btn-secondary {
    background: linear-gradient(135deg, var(--main-orange), var(--secondary-light-orange));
    color: white;
    box-shadow: 0 8px 25px rgba(255, 153, 51, 0.4);
}

.btn-secondary:hover {
    transform: translateY(-3px);
    box-shadow: 0 12px 35px rgba(255, 153, 51, 0.5);
}

.btn-primary span,
.btn-secondary span {
  a {
    all:unset;
  }
    position: relative;
    z-index: 2;
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(50px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Responsividade */
@media screen and (max-width: 1200px) {
    #banner {
        height: 65vh;
        min-height: 500px;
    }

    .main-title {
        font-size: 3rem;
    }

    .subtitle {
        font-size: 1.8rem;
    }
}

@media screen and (max-width: 768px) {
    #banner {
        height: 60vh;
        min-height: 450px;
    }

    #heading-container {
        padding: 0 30px;
    }

    .main-title {
        font-size: 2.5rem;
    }

    .subtitle {
        font-size: 1.5rem;
    }

    .description {
        font-size: 1.1rem;
    }

    #button-containers {
        gap: 15px;
    }

    .btn-primary,
    .btn-secondary {
        padding: 14px 28px;
        font-size: 1rem;
    }
}

@media screen and (max-width: 480px) {
    #banner {
        height: 60vh;
        min-height: 400px;
    }

    #heading-container {
        padding: 0 15px;
    }

    .main-title {
        font-size: 1.8rem;
        line-height: 1.2;
    }

    .subtitle {
        font-size: 1.2rem;
    }

    .description {
        font-size: 0.95rem;
        line-height: 1.5;
    }

    #button-containers {
        flex-direction: column;
        align-items: center;
        gap: 12px;
    }

    .btn-primary,
    .btn-secondary {
        width: 100%;
        max-width: 250px;
        padding: 14px 24px;
        font-size: 0.95rem;
    }
}

@media screen and (max-width: 360px) {
    #banner {
        height: 55vh;
        min-height: 350px;
    }

    .main-title {
        font-size: 1.6rem;
    }

    .subtitle {
        font-size: 1.1rem;
    }

    .description {
        font-size: 0.9rem;
    }
}
</style>
