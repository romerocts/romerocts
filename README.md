/* 1. BASE Y TIPOGRAFÍA (Reset & Variables) */
:root {
    --color-primary: #007bff; /* Azul de acento vibrante */
    --color-secondary: #ff6b6b; /* Rojo suave para CTA secundario */
    --color-text-dark: #1a1a1a;
    --color-bg-light: #f8f8fb; 
    --font-family: 'Poppins', sans-serif;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: var(--font-family);
    line-height: 1.6;
    color: var(--color-text-dark);
    background-color: #fff; /* Fondo blanco puro */
}

/* Utilidades de Contenedor y Espaciado */
.container {
    width: 85%;
    max-width: 1200px;
    margin: 0 auto;
}

.py-12 { padding-top: 4rem; padding-bottom: 4rem; }
.py-20 { padding-top: 6rem; padding-bottom: 6rem; }
.text-center { text-align: center; }

/* Botones (CTAs) */
.cta-button {
    display: inline-block;
    padding: 12px 30px;
    border: none;
    cursor: pointer;
    text-transform: uppercase;
    letter-spacing: 1px;
    transition: all 0.3s ease; /* Transición suave, clave del diseño moderno */
}

/* Botón Principal (Primary) */
.cta-button.primary {
    background-color: var(--color-primary);
    color: white;
    border: 2px solid var(--color-primary);
}
.cta-button.primary:hover {
    transform: translateY(-3px); /* Efecto de levitación */
    box-shadow: 0 8px 15px rgba(0, 123, 255, 0.2);
    background-color: #0056b3;
}

/* Botón Secundario (Secondary) */
.cta-button.secondary {
    background-color: transparent;
    border: 2px solid var(--color-text-dark);
    color: var(--color-text-dark);
}
.cta-button.secondary:hover {
    background-color: var(--color-text-dark);
    color: white;
}


/* ========================== SECCIÓN 1: HEADER ========================== */
.main-header {
    position: sticky; /* ¡CLAVE! Navbar que se queda pegado al scroll */
    top: 0;
    background: rgba(255, 255, 255, 0.9); /* Fondo semi-transparente para el efecto moderno */
    box-shadow: 0 1px 10px rgba(0, 0, 0, 0.05);
    z-index: 100;
}

.header-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0;
}

.logo {
    font-size: 1.8rem;
    font-weight: 800; /* Audaz */
    text-decoration: none;
    color: var(--color-text-dark);
}

nav ul {
    list-style: none;
    display: flex;
    gap: 30px;
}

nav a {
    text-decoration: none;
    color: var(--color-text-dark);
    font-weight: 600;
    transition: color 0.3s;
}
nav a:hover {
    color: var(--color-primary);
}

/* ========================== SECCIÓN 2: HERO ========================== */
.hero-section {
    height: 80vh; /* Ocupa la mayor parte de la vista */
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

/* El fondo debe estar por debajo del contenido, pero lo superponemos con posicionamiento absoluto */
.hero-background {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%; 
    background-size: cover;
    background-position: center;
    filter: brightness(0.8); /* Oscurece ligeramente la imagen para que el texto resalte */
}

.hero-content {
    z-index: 10; /* Asegura que el contenido esté visible sobre la imagen */
    max-width: 700px;
}

.hero-content h1 {
    font-size: 4rem;
    margin-bottom: 15px;
    font-weight: 800; /* Muy audaz */
}

.subheadline {
    font-size: 1.2rem;
    color: #666;
    margin-bottom: 30px;
}


/* ========================== SECCIÓN 3: PRODUCTOS (GRID ASIMÉTRICO) ========================== */
.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px; /* Espacio uniforme entre productos */
}

.product-card {
    background: #fff;
    overflow: hidden;
    cursor: pointer;
    transition: transform 0.3s ease;
}
/* Efecto de hover moderno en la tarjeta completa */
.hover-effect:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1) !important;
}

.product-card img {
    width: 100%;
    height: 350px; /* Altura fija para uniformidad visual */
    object-fit: cover;
    display: block;
}

/* Estilo de Producto grande (El toque creativo) */
.large-item {
    grid-column: span 2; /* Hace que este producto ocupe dos columnas */
    display: flex;
    flex-direction: column;
    position: relative;
}

.overlay-text {
    background: var(--color-primary);
    color: white;
    padding: 30px;
    transform: translateY(100%); /* Inicialmente oculto */
    transition: transform 0.5s ease;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
/* JS debe añadir la clase 'active' para que esto funcione con el hover o scroll */


/* ========================== SECCIÓN 4 & 5 (VALUE PROPOSITION & CTA) ========================== */
.bg-light { background-color: var(--color-bg-light); }

.flex
