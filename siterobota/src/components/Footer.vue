<script setup>
</script>

<template>
    <footer id="main-container">
        <div class="footer-content">
            <div class="footer-info">
                <div class="footer-logo">
                    <img src="../assets/robota_logo.svg" alt="ROBOTA Logo">
                    <h3>ROBOTA</h3>
                </div>
                <p class="footer-description">
                    Equipe de Robótica da UFSC desenvolvendo tecnologias inovadoras desde 2002
                </p>
            </div>
            
            <div class="footer-links">
                <div class="link-section">
                    <h4>Navegação</h4>
                    <ul>
                        <li><a href="#inicio">Início</a></li>
                        <li><a href="#sobre">Sobre nós</a></li>
                        <li><a href="#equipes">Equipes</a></li>
                        <li><a href="#servicos">Serviços</a></li>
                        <li><a href="#contato">Contato</a></li>
                    </ul>
                </div>
                
                <div class="link-section">
                    <h4>Projetos</h4>
                    <ul>
                        <li><a href="#trekking">Trekking</a></li>
                        <li><a href="#combate">Combate</a></li>
                        <li><a href="#seguidor">Seguidor de Linha</a></li>
                    </ul>
                </div>
                
                <div class="link-section">
                    <h4>Redes Sociais</h4>
                    <div class="social-links">
                        <a href="https://www.instagram.com/robota.ufsc/" class="social-link" target="_blank" rel="noopener noreferrer">
                            <img src="../assets/icons8-instagram.svg" alt="Instagram">
                        </a>
                        <a href="#" class="social-link">
                            <img src="../assets/icons8-facebook.svg" alt="Facebook">
                        </a>
                        <a href="#" class="social-link">
                            <img src="../assets/icons8-tiktok.svg" alt="TikTok">
                        </a>
                        <a href="#" class="social-link">
                            <img src="../assets/icons8-twitter.svg" alt="Twitter">
                        </a>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="footer-bottom">
            <div class="copyright">
                <p><strong>ROBOTA 2002-2025</strong> | Todos os direitos reservados</p>
                <p class="university">Universidade Federal de Santa Catarina - UFSC</p>
            </div>
        </div>
    </footer>
</template>

<style scoped>
#main-container {
    background: linear-gradient(135deg, var(--secondary-dark-purple), var(--main-purple));
    color: white;
    padding: 60px 0 20px 0;
    margin-top: 80px;
}

.footer-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    display: grid;
    grid-template-columns: 1fr 2fr;
    gap: 60px;
    align-items: start;
}

.footer-info {
    .footer-logo {
        display: flex;
        align-items: center;
        gap: 15px;
        margin-bottom: 20px;
        
        img {
            width: 50px;
            height: 50px;
            filter: brightness(0) invert(1);
        }
        
        h3 {
            font-size: 28px;
            font-weight: 700;
            background: linear-gradient(45deg, var(--main-yellow), var(--main-orange));
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    }
    
    .footer-description {
        font-size: 16px;
        line-height: 1.6;
        opacity: 0.9;
        max-width: 300px;
    }
}

.footer-links {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 40px;
}

.link-section {
    h4 {
        font-size: 18px;
        font-weight: 600;
        margin-bottom: 20px;
        color: var(--main-yellow);
    }
    
    ul {
        list-style: none;
        padding: 0;
        margin: 0;
        
        li {
            margin-bottom: 12px;
            
            a {
                color: rgba(255, 255, 255, 0.8);
                text-decoration: none;
                font-size: 14px;
                transition: all 0.3s ease;
                
                &:hover {
                    color: var(--main-orange);
                    transform: translateX(5px);
                }
            }
        }
    }
}

.social-links {
    display: flex;
    gap: 15px;
    
    .social-link {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 40px;
        height: 40px;
        background: rgba(255, 255, 255, 0.1);
        border-radius: 50%;
        transition: all 0.3s ease;
        
        img {
            width: 20px;
            height: 20px;
            filter: brightness(0) invert(1);
        }
        
        &:hover {
            background: linear-gradient(45deg, var(--main-orange), var(--main-yellow));
            transform: translateY(-3px);
        }
    }
}

.footer-bottom {
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    margin-top: 40px;
    padding-top: 30px;
    
    .copyright {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 20px;
        text-align: center;
        
        p {
            margin: 5px 0;
            font-size: 14px;
            opacity: 0.8;
            
            &.university {
                font-size: 12px;
                opacity: 0.6;
            }
        }
    }
}

@media screen and (max-width: 1200px) {
    .footer-content {
        padding: 0 30px;
        gap: 50px;
    }
}

@media screen and (max-width: 768px) {
    #main-container {
        padding: 50px 0 20px 0;
    }
    
    .footer-content {
        grid-template-columns: 1fr;
        gap: 40px;
        text-align: center;
        padding: 0 20px;
    }
    
    .footer-info {
        .footer-logo {
            justify-content: center;
            
            h3 {
                font-size: 24px;
            }
        }
        
        .footer-description {
            font-size: 0.95rem;
            line-height: 1.6;
        }
    }
    
    .footer-links {
        grid-template-columns: 1fr;
        gap: 30px;
        
        .link-section {
            h4 {
                font-size: 1.2rem;
            }
            
            ul li a {
                font-size: 0.95rem;
            }
        }
    }
    
    .social-links {
        justify-content: center;
        gap: 15px;
    }
    
    .footer-bottom .copyright {
        p {
            font-size: 0.9rem;
        }
        
        .university {
            font-size: 0.85rem;
        }
    }
}

@media screen and (max-width: 480px) {
    #main-container {
        padding: 40px 0 15px 0;
    }
    
    .footer-content {
        padding: 0 15px;
        gap: 35px;
    }
    
    .footer-info {
        .footer-logo {
            img {
                width: 40px;
                height: 40px;
            }
            
            h3 {
                font-size: 20px;
            }
        }
        
        .footer-description {
            font-size: 0.9rem;
        }
    }
    
    .footer-links {
        gap: 25px;
        
        .link-section {
            h4 {
                font-size: 1.1rem;
                margin-bottom: 12px;
            }
            
            ul li {
                margin-bottom: 8px;
                
                a {
                    font-size: 0.9rem;
                }
            }
        }
    }
    
    .social-links {
        gap: 12px;
        
        .social-link {
            width: 40px;
            height: 40px;
            
            img {
                width: 20px;
                height: 20px;
            }
        }
    }
    
    .footer-bottom {
        padding-top: 20px;
        
        .copyright {
            p {
                font-size: 0.85rem;
            }
            
            .university {
                font-size: 0.8rem;
            }
        }
    }
}

@media screen and (max-width: 360px) {
    .footer-info .footer-logo h3 {
        font-size: 18px;
    }
    
    .footer-bottom .copyright p {
        font-size: 0.8rem;
    }
}
</style>