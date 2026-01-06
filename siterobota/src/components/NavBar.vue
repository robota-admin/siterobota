<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
    <nav id="main-container">
        <div id="header">
            <div id="nav-logo">
                <a href="#inicio" class="logo-link">
                    <img src="../assets/robota_logo.svg" alt="ROBOTA Logo">
                    <h1>ROBOTA</h1>
                </a>
            </div>

            <div class="nav-content">
                <div id="nav-elements" :class="{ 'menu-open': isMenuOpen }">
                    <ul>
                        <li><a href="#">Início</a></li>
                        <li><a href="#main-container-sobre">Sobre nós</a></li>
                        <li><a href="#main-container-equipes">Equipes</a></li>
                        <li><a href="#main-container-servicos">Serviços</a></li>
                        <li><a href="#main-container-contato">Contato</a></li>
                    </ul>
                </div>

                <div id="nav-redes-sociais">
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

                <button class="menu-toggle" @click="toggleMenu" :class="{ 'active': isMenuOpen }">
                    <span></span>
                    <span></span>
                    <span></span>
                </button>
            </div>
        </div>
    </nav>
</template>

<style scoped>
#main-container {
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid rgba(102, 51, 153, 0.1);
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
}

#header {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 80px;
}

#nav-logo {
    .logo-link {
        display: flex;
        align-items: center;
        gap: 12px;
        text-decoration: none;
        color: inherit;
        transition: all 0.3s ease;

        &:hover {
            transform: translateY(-2px);
        }

        img {
            width: 50px;
            height: 50px;
            transition: all 0.3s ease;
        }

        h1 {
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(135deg, var(--main-purple), var(--main-orange));
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 0;
        }

        &:hover img {
            transform: rotate(5deg) scale(1.1);
        }
    }
}

.nav-content {
    display: flex;
    align-items: center;
    gap: 30px;
}

#nav-elements {
    ul {
        list-style: none;
        display: flex;
        gap: 30px;
        margin: 0;
        padding: 0;

        li {
            a {
                text-decoration: none;
                color: var(--secondary-dark-purple);
                font-size: 1rem;
                font-weight: 500;
                padding: 10px 16px;
                border-radius: 25px;
                transition: all 0.3s ease;
                position: relative;

                &:hover {
                    background: linear-gradient(135deg, var(--main-purple), var(--main-orange));
                    color: white;
                    transform: translateY(-2px);
                    box-shadow: 0 5px 15px rgba(102, 51, 153, 0.3);
                }

                &::after {
                    content: '';
                    position: absolute;
                    bottom: -5px;
                    left: 50%;
                    width: 0;
                    height: 2px;
                    background: linear-gradient(90deg, var(--main-purple), var(--main-orange));
                    transition: all 0.3s ease;
                    transform: translateX(-50%);
                }

                &:hover::after {
                    width: 100%;
                }
            }
        }
    }
}

#nav-redes-sociais {
    display: flex;
    gap: 12px;

    .social-link {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background: rgba(102, 51, 153, 0.1);
        transition: all 0.3s ease;

        img {
            width: 20px;
            height: 20px;
            opacity: 0.7;
            transition: all 0.3s ease;
        }

        &:hover {
            background: linear-gradient(135deg, var(--main-purple), var(--main-orange));
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(102, 51, 153, 0.3);

            img {
                opacity: 1;
                filter: brightness(0) invert(1);
            }
        }
    }
}

.menu-toggle {
    display: none;
    flex-direction: column;
    background: none;
    border: none;
    cursor: pointer;
    padding: 5px;

    span {
        width: 25px;
        height: 3px;
        background: var(--main-purple);
        margin: 3px 0;
        transition: all 0.3s ease;
        border-radius: 2px;
    }

    &.active span:nth-child(1) {
        transform: rotate(45deg) translate(5px, 5px);
    }

    &.active span:nth-child(2) {
        opacity: 0;
    }

    &.active span:nth-child(3) {
        transform: rotate(-45deg) translate(7px, -6px);
    }
}

@media screen and (max-width: 768px) {
    #header {
        padding: 0 15px;
        height: 70px;
    }

    #nav-logo .logo-link {
        h1 {
            font-size: 1.4rem;
        }

        img {
            width: 40px;
            height: 40px;
        }
    }

    .nav-content {
        gap: 15px;
    }

    .menu-toggle {
        display: flex;
        order: 2;
    }

    #nav-redes-sociais {
        display: none;
    }

    #nav-elements {
        position: absolute;
        top: 100%;
        left: 0;
        right: 0;
        background: white;
        box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        border-top: 1px solid rgba(102, 51, 153, 0.1);
        transform: translateY(-100%);
        opacity: 0;
        visibility: hidden;
        transition: all 0.3s ease;

        &.menu-open {
            transform: translateY(0);
            opacity: 1;
            visibility: visible;
        }

        ul {
            flex-direction: column;
            gap: 0;
            padding: 20px;

            li {
                width: 100%;

                a {
                    display: block;
                    padding: 15px 20px;
                    border-radius: 8px;
                    text-align: center;

                    &::after {
                        display: none;
                    }
                }
            }
        }
    }

    #nav-redes-sociais {
        gap: 8px;

        .social-link {
            width: 35px;
            height: 35px;

            img {
                width: 18px;
                height: 18px;
            }
        }
    }
}

@media screen and (max-width: 480px) {
    #header {
        padding: 0 10px;
        height: 65px;
    }

    #nav-logo .logo-link {
        h1 {
            font-size: 1.2rem;
        }

        img {
            width: 35px;
            height: 35px;
        }
    }

    #nav-redes-sociais {
        gap: 6px;

        .social-link {
            width: 32px;
            height: 32px;

            img {
                width: 16px;
                height: 16px;
            }
        }
    }

    .menu-toggle {
        span {
            width: 22px;
            height: 2px;
        }
    }
}

@media screen and (max-width: 1200px) {
    #main-container {
        margin-left: 0;
        margin-right: 0;
    }
}
</style>
