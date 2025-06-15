<script setup>
</script>

<template>
    <div id="main-container">
        <div class="section-header">
            <h2>QUEM SOMOS</h2>
            <div class="accent-line"></div>
        </div>
        
        <div class="hero-section">
            <h3 class="hero-title">ROBOTA - Equipe de Robótica da UFSC</h3>
            <p class="hero-description">
                A ROBOTA é uma equipe de robótica móvel vinculada à Universidade Federal de Santa Catarina (UFSC) 
                que atua há mais de duas décadas no desenvolvimento de projetos competitivos. Desde 2002, o grupo 
                se dedica à criação e aperfeiçoamento de robôs autônomos para diversas modalidades de competição.
            </p>
        </div>

        <div class="content-grid">
            <div class="mission-card">
                <h4>Missão e Objetivos</h4>
                <p>
                    A ROBOTA combina conhecimento acadêmico com aplicação prática, proporcionando aos estudantes 
                    da UFSC uma experiência única no desenvolvimento de sistemas robóticos. O grupo contribui para 
                    o avanço da robótica nacional através da participação em competições e do desenvolvimento de 
                    tecnologias inovadoras.
                </p>
                <p>
                    A equipe representa não apenas um projeto de extensão universitária, mas também um centro de 
                    formação de profissionais qualificados na área de robótica e automação, preparando os estudantes 
                    para os desafios tecnológicos do futuro.
                </p>
            </div>
            
            <div class="stats-section">
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-icon">📅</div>
                        <h4>20+</h4>
                        <p>anos de existência</p>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon">👥</div>
                        <h4>30+</h4>
                        <p>membros ativos</p>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon">🤖</div>
                        <h4>7+</h4>
                        <p>robôs desenvolvidos</p>
                    </div>
                    <div class="stat-card">
                        <div class="stat-icon">🏆</div>
                        <h4>7+</h4>
                        <p>competições disputadas</p>
                    </div>
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
    background: linear-gradient(135deg, rgba(102, 51, 153, 0.05) 0%, rgba(255, 204, 102, 0.05) 100%);
}

.section-header {
    text-align: center;
    margin-bottom: 60px;
}

.section-header h2 {
    font-size: 3rem;
    font-weight: 800;
    color: var(--main-purple);
    margin: 0 0 20px 0;
    letter-spacing: -0.02em;
}

.accent-line {
    width: 80px;
    height: 4px;
    background: linear-gradient(90deg, var(--main-orange), var(--main-yellow));
    margin: 0 auto;
    border-radius: 2px;
}

.hero-section {
    text-align: center;
    margin-bottom: 80px;
    background: white;
    padding: 60px 40px;
    border-radius: 20px;
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
    border: 1px solid rgba(102, 51, 153, 0.1);
}

.hero-title {
    font-size: 2.5rem;
    font-weight: 700;
    color: var(--main-purple);
    margin: 0 0 30px 0;
    background: linear-gradient(135deg, var(--main-purple), var(--secondary-light-purple));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.hero-description {
    font-size: 1.2rem;
    line-height: 1.8;
    color: #555;
    max-width: 800px;
    margin: 0 auto;
}

.content-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    align-items: start;
}

.mission-card {
    background: white;
    padding: 50px 40px;
    border-radius: 20px;
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08);
    border: 1px solid rgba(102, 51, 153, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.mission-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 25px 60px rgba(0, 0, 0, 0.15);
}

.mission-card h4 {
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--main-purple);
    margin: 0 0 25px 0;
    position: relative;
}

.mission-card h4::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 0;
    width: 40px;
    height: 3px;
    background: var(--main-orange);
    border-radius: 2px;
}

.mission-card p {
    font-size: 1.1rem;
    line-height: 1.7;
    color: #666;
    margin-bottom: 20px;
}

.stats-section {
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
}

.stat-card {
    background: white;
    padding: 30px 20px;
    border-radius: 16px;
    text-align: center;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
    border: 1px solid rgba(102, 51, 153, 0.1);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
}

.stat-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--main-purple), var(--main-orange), var(--main-yellow));
}

.stat-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.stat-icon {
    font-size: 2.5rem;
    margin-bottom: 15px;
}

.stat-card h4 {
    font-size: 2.2rem;
    font-weight: 800;
    color: var(--main-purple);
    margin: 0 0 8px 0;
}

.stat-card p {
    font-size: 1rem;
    color: #666;
    margin: 0;
    font-weight: 500;
}

/* Responsividade */
@media screen and (max-width: 1200px) {
    #main-container {
        padding: 60px 30px;
    }
    
    .content-grid {
        gap: 30px;
    }
}

@media screen and (max-width: 768px) {
    #main-container {
        padding: 50px 20px;
    }
    
    .section-header h2 {
        font-size: 2.2rem;
    }
    
    .hero-title {
        font-size: 1.8rem;
    }
    
    .hero-description {
        font-size: 1.05rem;
    }
    
    .content-grid {
        grid-template-columns: 1fr;
        gap: 25px;
    }
    
    .hero-section {
        padding: 40px 25px;
        margin-bottom: 50px;
    }
    
    .mission-card {
        padding: 35px 25px;
    }
    
    .mission-card h4 {
        font-size: 1.6rem;
    }
    
    .mission-card p {
        font-size: 1rem;
    }
    
    .stats-grid {
        grid-template-columns: repeat(2, 1fr);
        gap: 15px;
    }
    
    .stat-card {
        padding: 25px 15px;
    }
    
    .stat-card h4 {
        font-size: 2rem;
    }
}

@media screen and (max-width: 480px) {
    #main-container {
        padding: 40px 15px;
    }
    
    .section-header h2 {
        font-size: 1.8rem;
    }
    
    .hero-title {
        font-size: 1.5rem;
    }
    
    .hero-description {
        font-size: 1rem;
    }
    
    .hero-section {
        padding: 30px 20px;
        margin-bottom: 40px;
    }
    
    .mission-card {
        padding: 25px 20px;
    }
    
    .mission-card h4 {
        font-size: 1.4rem;
    }
    
    .stats-grid {
        grid-template-columns: 1fr;
        gap: 12px;
    }
    
    .stat-card {
        padding: 20px 15px;
    }
    
    .stat-icon {
        font-size: 2rem;
    }
    
    .stat-card h4 {
        font-size: 1.8rem;
    }
}

@media screen and (max-width: 360px) {
    .section-header h2 {
        font-size: 1.6rem;
    }
    
    .hero-title {
        font-size: 1.3rem;
    }
    
    .mission-card h4 {
        font-size: 1.2rem;
    }
}
</style>
