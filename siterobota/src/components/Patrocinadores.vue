<script setup>
</script>

<template>
    <div id="main-container">
        <div class="section-header">
            <h2>PATROCINADORES</h2>
            <div class="accent-line"></div>
            <p class="section-description">
                Apoie a inovação em robótica e faça parte da nossa história
            </p>
        </div>
        
        <div id="patrocinadores">
            <div class="sponsor-placeholder">
                <div class="sponsor-card">
                    <div class="sponsor-icon">🤝</div>
                    <h3>Seja nosso parceiro</h3>
                    <p>Entre em contato conosco para conhecer nossas oportunidades de patrocínio</p>
                    <button class="btn-primary">Patrocinar</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
#main-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 80px 20px;
    text-align: center;
}

.section-header {
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

#patrocinadores {
    display: flex;
    justify-content: center;
    
    .sponsor-placeholder {
        max-width: 400px;
        
        .sponsor-card {
            background: white;
            padding: 50px 40px;
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08);
            border: 2px dashed rgba(102, 51, 153, 0.2);
            transition: all 0.3s ease;
            
            &:hover {
                transform: translateY(-5px);
                box-shadow: 0 25px 60px rgba(0, 0, 0, 0.15);
                border-color: var(--main-purple);
            }
            
            .sponsor-icon {
                font-size: 4rem;
                margin-bottom: 25px;
            }
            
            h3 {
                font-size: 1.8rem;
                font-weight: 700;
                color: var(--main-purple);
                margin: 0 0 20px 0;
            }
            
            p {
                font-size: 1.1rem;
                line-height: 1.6;
                color: #666;
                margin-bottom: 30px;
            }
            
            .btn-primary {
                background: linear-gradient(135deg, var(--main-purple), var(--secondary-light-purple));
                color: white;
                padding: 14px 28px;
                border: none;
                border-radius: 50px;
                font-weight: 600;
                cursor: pointer;
                transition: all 0.3s ease;
                text-transform: uppercase;
                letter-spacing: 0.5px;
                
                &:hover {
                    transform: translateY(-2px);
                    box-shadow: 0 8px 25px rgba(102, 51, 153, 0.4);
                }
            }
        }
    }
}

@media screen and (max-width: 1200px) {
    #main-container {
        padding: 60px 30px;
    }
}

@media screen and (max-width: 768px) {
    #main-container {
        padding: 50px 20px;
    }
    
    .section-header h2 {
        font-size: 2rem;
    }
    
    .section-header .section-description {
        font-size: 1rem;
    }
    
    .sponsor-card {
        padding: 35px 25px !important;
        
        .sponsor-icon {
            font-size: 3rem !important;
        }
        
        h3 {
            font-size: 1.4rem !important;
        }
        
        p {
            font-size: 0.95rem !important;
        }
        
        .btn-primary {
            padding: 12px 24px;
            font-size: 0.9rem;
        }
    }
}

@media screen and (max-width: 480px) {
    #main-container {
        padding: 40px 15px;
    }
    
    .section-header h2 {
        font-size: 1.8rem;
    }
    
    .sponsor-card {
        padding: 30px 20px !important;
        
        .sponsor-icon {
            font-size: 2.5rem !important;
        }
        
        h3 {
            font-size: 1.2rem !important;
        }
        
        p {
            font-size: 0.9rem !important;
            margin-bottom: 25px;
        }
        
        .btn-primary {
            padding: 10px 20px;
            font-size: 0.85rem;
        }
    }
}

@media screen and (max-width: 360px) {
    .section-header h2 {
        font-size: 1.6rem;
    }
    
    .sponsor-card h3 {
        font-size: 1.1rem !important;
    }
}
</style>