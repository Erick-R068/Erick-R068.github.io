<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portafolio | Erick Riquelme Yáñez</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .section-title {
            @apply text-3xl font-bold text-white mb-8;
        }
        .card {
            /* Estilo de tarjeta para modo oscuro */
            @apply bg-gray-900 rounded-lg shadow-xl overflow-hidden p-6 
                   border border-gray-700/50 
                   transition-all duration-300 
                   hover:transform hover:-translate-y-1 
                   hover:shadow-2xl hover:shadow-[var(--color-primary)]/20 
                   hover:border-[var(--color-primary)]/50;
        }
        /* Estilos para los tags de skills y tech, ahora usando variables CSS */
        .skill {
            /* Tags de skills genéricos */
            @apply inline-block bg-gray-700 text-gray-200 px-3 py-1 rounded-full text-sm font-semibold mr-2 mb-2;
        }
        .tech-tag {
            /* Tags de tecnología con color primario */
            @apply inline-block bg-[var(--color-primary-dark)] text-[var(--color-primary-light)] px-3 py-1 rounded-full text-xs font-semibold mr-2 mb-2;
        }

        /* Animación de Fade-in-Up */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .fade-in {
            animation: fadeInUp 0.6s cubic-bezier(0.215, 0.610, 0.355, 1.000) forwards;
            opacity: 0; /* Asegura que comience invisible */
        }
    </style>
</head>
<body class="bg-gray-950 text-gray-300">

    <!-- Header & Navigation con Efecto Glassmorphism -->
    <header class="bg-gray-950/70 shadow-lg backdrop-blur-lg sticky top-0 z-50 border-b border-gray-700/50">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <div class="text-2xl font-bold text-white">
                <a href="#" id="nav-name">Erick Riquelme Y.</a>
            </div>
            <div class="hidden md:flex space-x-6">
                <a href="#perfil" class="text-gray-300 hover:text-[var(--color-primary)]">Perfil</a>
                <a href="#proyectos" class="text-gray-300 hover:text-[var(--color-primary)]">Proyectos</a>
                <a href="#servicios" class="text-gray-300 hover:text-[var(--color-primary)]">Servicios</a>
                <a href="#experiencia" class="text-gray-300 hover:text-[var(--color-primary)]">Experiencia</a>
                <a href="#cv" class="text-gray-300 hover:text-[var(--color-primary)]">CV</a>
                <a href="#contacto" id="nav-contact" class="bg-[var(--color-primary)] text-white px-4 py-2 rounded-full hover:bg-[var(--color-primary-hover)] transition-colors">Contacto</a>
            </div>
            <!-- Mobile Menu Button (optional) -->
        </nav>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto px-6 py-12">

        <!-- Portada (Hero Section) -->
        <section id="portada" class="flex flex-col md:flex-row items-center justify-between py-16 md:py-24">
            <div class="md:w-2/3">
                <h1 id="hero-name" class="text-4xl md:text-6xl font-bold text-white mb-4">Erick Riquelme Yáñez</h1>
                <h2 id="hero-title" class="text-2xl md:text-3xl font-semibold text-[var(--color-primary)] mb-6">Ingeniero de Software (Backend & Cloud)</h2>
                
                <!-- Datos de Contacto -->
                <div class="flex flex-wrap gap-4 text-lg">
                    <a id="hero-email" href="mailto:erick.riquelme.y@gmail.com" class="flex items-center text-gray-300 hover:text-[var(--color-primary)]">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" /></svg>
                        <span id="hero-email-text">erick.riquelme.y@gmail.com</span>
                    </a>
                    <a id="hero-linkedin" href="https://linkedin.com/in/erick-riquelme-y" target="_blank" class="flex items-center text-gray-300 hover:text-[var(--color-primary)]">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.784-1.75-1.75s.784-1.75 1.75-1.75 1.75.784 1.75 1.75-.784 1.75-1.75 1.75zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
                        LinkedIn
                    </a>
                    <a id="hero-github" href="https://github.com/tu-usuario" target="_blank" class="flex items-center text-gray-300 hover:text-[var(--color-primary)]"> <!-- REEMPLAZAR LINK -->
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.108-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.d.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                        GitHub
                    </a>
                </div>
            </div>
            <!-- Foto Profesional (Opcional) -->
            <div class="md:w-1/3 mt-10 md:mt-0 flex justify-center">
                <img id="hero-image" src="https://placehold.co/300x300/EBF8FF/3182CE?text=Foto+(Opcional)" alt="Foto Profesional" class="rounded-full shadow-lg w-64 h-64 md:w-80 md:h-80 object-cover">
            </div>
        </section>

        <!-- Perfil Profesional y Habilidades -->
        <section id="perfil" class="py-16">
            <h3 class="section-title">Perfil Profesional</h3>
            <p id="profile-summary" class="text-lg text-gray-300 leading-relaxed max-w-4xl mb-12">
                Ingeniero de Software con +1 año de experiencia, especializado en desarrollo Backend con Python y arquitectura Cloud (GCP/AWS). Experto en la migración de sistemas legacy y el diseño de orquestaciones de datos escalables. Demostrada capacidad para liderar proyectos de IA (Vertex AI) y optimizar el rendimiento de APIs para alta concurrencia. Busco aplicar mi *expertise* técnico para resolver desafíos de datos complejos.
            </p>

            <h3 class="text-2xl font-bold text-white mb-6">Competencias</h3>
            <!-- Contenedor para habilidades generadas por JS -->
            <div id="skills-container" class="space-y-4">
                <!-- Las habilidades se insertarán aquí dinámicamente -->
            </div>
        </section>

        <!-- Proyectos Destacados (Mínimo 3) -->
        <section id="proyectos" class="py-16 bg-gray-900 -mx-6 px-6">
            <h3 class="section-title">Proyectos Destacados</h3>
            <!-- Contenedor para proyectos generados por JS -->
            <div id="projects-container" class="grid md:grid-cols-3 gap-8">
                <!-- Los proyectos se insertarán aquí dinámicamente -->
            </div>
        </section>

        <!-- Servicios que puedes ofrecer -->
        <section id="servicios" class="py-16">
            <h3 class="section-title">Servicios que Puedo Ofrecer</h3>
            <!-- Contenedor para servicios generados por JS -->
            <div id="services-container" class="grid md:grid-cols-3 gap-8">
                <!-- Los servicios se insertarán aquí dinámicamente -->
            </div>
        </section>

        <!-- Experiencia Profesional -->
        <section id="experiencia" class="py-16 bg-gray-900 -mx-6 px-6">
            <h3 class="section-title">Experiencia Profesional</h3>
            <!-- Contenedor para experiencia generada por JS -->
            <div id="experience-container" class="space-y-8">
                <!-- La experiencia se insertará aquí dinámicamente -->
            </div>
        </section>

        <!-- Certificaciones, Cursos y Reconocimientos -->
        <section id="certificaciones" class="py-16">
            <h3 class="section-title">Educación y Certificaciones</h3>
            <div class="grid md:grid-cols-2 gap-8">
                <div class="card">
                    <h4 id="education-title" class="font-bold text-xl text-white mb-2">Ingeniería en Computación e Informática</h4>
                    <p id="education-institution" class="font-semibold text-lg text-gray-300">Universidad Andrés Bello | Santiago, Chile</p>
                    <p id="education-period" class="text-gray-400">Finaliza en 2025</p>
                </div>
                <div class="card">
                    <h4 class="font-bold text-xl text-white mb-2">Certificaciones Oficiales</h4>
                    <!-- Contenedor para certificaciones generadas por JS -->
                    <ul id="certs-list" class="list-disc list-inside text-gray-300 space-y-1">
                        <!-- Las certificaciones se insertarán aquí dinámicamente -->
                    </ul>
                </div>
            </div>
        </section>

        <!-- Currículum Vitae (Sección) -->
        <section id="cv" class="py-16 bg-gray-950 -mx-6 px-6 text-center">
            <h3 class="section-title">Currículum Vitae</h3>
            <p class="text-lg text-gray-300 mb-8">Aquí puedes ver un resumen de mi CV. Para un desglose completo, recomiendo revisar las secciones de este portafolio.</p>
            <!-- Opcional: Botón de descarga -->
            <!-- <a id="cv-download-button" href="CV_Erick_Riquelme.pdf" download class="bg-[var(--color-primary)] text-white px-6 py-3 rounded-full hover:bg-[var(--color-primary-hover)] transition-colors font-semibold">
                Descargar CV en PDF
            </a> -->

            <!-- CV Embebido (versión corta) -->
            <div class="text-left max-w-4xl mx-auto bg-gray-900 p-8 rounded-lg shadow-xl border border-gray-700/50 mt-8">
                <h4 id="cv-name" class="font-bold text-2xl text-center text-white mb-6">ERICK RIQUELME YÁÑEZ</h4>
                <p id="cv-title" class="text-center font-semibold text-xl text-[var(--color-primary)] mb-6">Ingeniero de Software (Backend & Cloud)</p>
                
                <h5 class="font-bold text-lg text-white mt-4 mb-2">PERFIL PROFESIONAL</h5>
                <p id="cv-summary" class="text-sm text-gray-300">Ingeniero de Software con +1 año de experiencia, especializado en desarrollo Backend con Python y arquitectura Cloud (GCP/AWS). Experto en la migración de sistemas legacy...</p>
                
                <h5 class="font-bold text-lg text-white mt-4 mb-2">EXPERIENCIA</h5>
                <p id="cv-exp1-title" class="text-sm text-gray-300"><strong>Software Engineer (Backend & Cloud)</strong> | Equifax (vía 23people) | Ene 2025 – Presente</p>
                <ul id="cv-exp1-list" class="list-disc list-inside text-sm text-gray-300 pl-4">
                    <li>Lideré la refactorización y migración de servicios legacy (.NET/SQL/C++)...</li>
                </ul>
                <p id="cv-exp2-title" class="text-sm text-gray-300 mt-2"><strong>Desarrollador Full Stack (Cloud)</strong> | Multicloud-X | Mar 2024 – Dic 2024</p>
                <ul id="cv-exp2-list" class="list-disc list-inside text-sm text-gray-300 pl-4">
                    <li>Desarrollé e integré APIs RESTful y asíncronas...</li>
                </ul>

                <h5 class="font-bold text-lg text-white mt-4 mb-2">PROYECTOS</h5>
                <p id="cv-proj1-title" class="text-sm text-gray-300"><strong>QuickFlow (Asistente Virtual con IA)</strong> | Desarrollador Líder | Abr 2025 – Oct 2025</p>
                <ul id="cv-proj1-list" class="list-disc list-inside text-sm text-gray-300 pl-4">
                    <li>Dirigí el desarrollo de un chatbot empresarial en GCP utilizando Gemini (Vertex AI)...</li>
                </ul>

                <h5 class="font-bold text-lg text-white mt-4 mb-2">EDUCACIÓN E IDIOMAS</h5>
                <p id="cv-edu" class="text-sm text-gray-300"><strong>Ingeniería en Computación e Informática</strong> | Universidad Andrés Bello (Finaliza 2025)</p>
                <p id="cv-lang" class="text-sm text-gray-300"><strong>Idiomas:</strong> Español (Nativo), Inglés (Nivel C2)</p>
            </div>
        </section>


        <!-- Carta de Presentación -->
        <section id="carta" class="py-16">
            <h3 class="section-title">Carta de Presentación General</h3>
            <div class="max-w-4xl mx-auto bg-gray-900 p-8 rounded-lg shadow-xl border border-gray-700/50">
                <p id="letter-date" class="text-gray-400 mb-4">20 de octubre de 2025</p>
                <p id="letter-greeting" class="font-semibold text-white mb-4">Estimado Equipo de Contratación,</p>
                
                <p id="letter-p1" class="text-gray-300 leading-relaxed mb-4">
                    Le escribo para expresar mi gran interés en posiciones de Software Engineer. Como Ingeniero de Software especializado en desarrollo Backend y arquitectura Cloud (GCP/AWS), mi experiencia en la migración de servicios legacy y el diseño de soluciones de datos escalables se alinea perfectamente con los desafíos de roles en su empresa.
                </pos>
                <p id="letter-p2" class="text-gray-300 leading-relaxed mb-4">
                    En mi rol actual como Software Engineer en Equifax, lidero la refactorización de servicios .NET y C++ a arquitecturas modernas en Python, diseñando e implementando orquestaciones de datos críticas. Mi capacidad para optimizar sistemas quedó demostrada en mi proyecto "QuickFlow", un asistente virtual basado en Gemini (Vertex AI) y RAG, donde desarrollé una API RESTful en Python capaz de gestionar altas cargas de consultas mediante Redis y Celery.
                </p>
                <p id="letter-p3" class="text-gray-300 leading-relaxed mb-4">
                    Mi objetivo es aplicar mi experiencia técnica en Python, GCP y Vertex AI para construir y optimizar sistemas de backend que impulsen soluciones innovadoras. La oportunidad de contribuir a su equipo y resolver desafíos de datos a gran escala es exactamente el siguiente paso que busco en mi carrera.
                </p>
                <p id="letter-p4" class="text-gray-300 leading-relaxed mb-4">
                    Estoy convencido de que mi perfil técnico y mi capacidad de autoaprendizaje me permitirían aportar un valor significativo.
                </p>
                <p id="letter-signoff" class="text-gray-300 leading-relaxed mt-6">
                    Atentamente,
                </p>
                <p id="letter-name" class="font-semibold text-white">Erick Riquelme Yáñez</p>
            </div>
        </section>

    </main>

    <!-- Footer (Contacto) -->
    <footer id="contacto" class="bg-gray-950 border-t border-gray-700/50">
        <div class="container mx-auto px-6 py-12 text-center">
            <h3 class="text-3xl font-bold text-white mb-4">Contacto</h3>
            <p class="text-lg text-gray-300 mb-8">Si mi perfil es de su interés, no dude en contactarme.</p>
            <div class="flex justify-center space-x-8">
                <a id="footer-email" href="mailto:erick.riquelme.y@gmail.com" class="text-gray-300 hover:text-[var(--color-primary)] text-lg">
                    erick.riquelme.y@gmail.com
                </a>
                <a id="footer-linkedin" href="https://linkedin.com/in/erick-riquelme-y" target="_blank" class="text-gray-300 hover:text-[var(--color-primary)] text-lg">
                    LinkedIn
                </a>
                <a id="footer-github" href="https://github.com/tu-usuario" target="_blank" class="text-gray-300 hover:text-[var(--color-primary)] text-lg"> <!-- REEMPLAZAR LINK -->
                    GitHub
                </a>
            </div>
            <p id="footer-copyright" class="text-gray-500 mt-12">&copy; 2025 Erick Riquelme Yáñez. Todos los derechos reservados.</p>
        </div>
    </footer>

    <!-- CSS para Skills y Tech Tags (para no repetir clases) -->
    <style>
        /* Estos estilos ya están definidos en el <head> para mejor performance, 
           pero se mantienen aquí como referencia de las clases usadas dinámicamente. */
        /*
        .skill {
            @apply inline-block bg-gray-700 text-gray-200 px-3 py-1 rounded-full text-sm font-semibold mr-2 mb-2;
        }
        .tech-tag {
            @apply inline-block bg-[var(--color-primary-dark)] text-[var(--color-primary-light)] px-3 py-1 rounded-full text-xs font-semibold mr-2 mb-2;
        }
        */
    </style>


    <!-- =================================================================== -->
    <!-- CONFIGURACIÓN DEL PORTAFOLIO                                        -->
    <!-- Edita el contenido de tu portafolio aquí.                         -->
    <!-- =================================================================== -->
    <script>
        const portfolioConfig = {
            // ----- PARÁMETROS DE PERFIL Y COLORES -----
            profile: {
                name: "Erick Riquelme Yáñez",
                title: "Ingeniero de Software (Backend & Cloud)",
                email: "erick.riquelme.y@gmail.com",
                linkedin: "https://linkedin.com/in/erick-riquelme-y",
                github: "https://github.com/tu-usuario", // <-- REEMPLAZA ESTO
                imageUrl: "https://placehold.co/300x300/EBF8FF/3182CE?text=Foto+(Opcional)", // URL de tu foto
                copyrightYear: "2025"
            },
            colors: {
                primary: "#2563EB",         // Azul (blue-600)
                primary_hover: "#1D4ED8",   // Azul oscuro (blue-700)
                primary_light: "#DBEAFE",   // Azul claro (blue-100)
                primary_dark: "#1E40AF"     // Azul más oscuro (blue-800)
            },

            // ----- CONTENIDO DE SECCIONES -----
            profileSummary: `Ingeniero de Software con +1 año de experiencia, especializado en desarrollo Backend con Python y arquitectura Cloud (GCP/AWS). Experto en la migración de sistemas legacy y el diseño de orquestaciones de datos escalables. Demostrada capacidad para liderar proyectos de IA (Vertex AI) y optimizar el rendimiento de APIs para alta concurrencia. Busco aplicar mi *expertise* técnico para resolver desafíos de datos complejos.`,
            
            skills: [
                { category: "Lenguajes", list: "Python (Experto), Javascript (Intermedio), C++ (Básico)" },
                { category: "Cloud & DevOps", list: "GCP (Cloud Digital Leader), AWS (Technical Accredited), Docker, Terraform" },
                { category: "Bases de Datos", list: "PostgreSQL, MongoDB, Redis" },
                { category: "Backend & Frameworks", list: "Flask, Celery, API RESTful, gRPC" },
                { category:T "IA & Datos", list: "Vertex AI Studio, RAG" },
                { category: "Frontend", list: "React (Básico)" },
                { category: "Metodologías", list: "Scrum, Design Thinking (Certificado)" }
            ],

            projects: [
                {
                    title: "QuickFlow (Asistente Virtual con IA)",
                    description: "Chatbot empresarial en GCP utilizando Gemini (Vertex AI) y técnicas RAG para la recuperación de información documental.",
                    role: "Desarrollador Líder",
                    results: "API RESTful en Python (Flask) optimizada para alta concurrencia, con caching en Redis y tareas asíncronas en Celery para reducir latencia.",
                    tags: ["GCP", "Vertex AI", "Python", "Flask", "Redis", "Celery"]
                },
                {
                    title: "DataPipe Legacy Migrator",
                    description: "Microservicio de orquestación para la migración de datos desde sistemas legacy (.NET/SQL) a una arquitectura moderna en GCP.",
                    role: "Ingeniero Backend",
                    results: "Automatización del 100% de la ingesta de datos, reduciendo errores manuales y mejorando la fiabilidad del servicio de consumo de datos.",
                    tags: ["Python", "GCP", "Cloud Functions", "Pub/Sub", ".NET", "SQL"]
                },
                {
                    title: "CloudOps Dashboard (Full Stack)",
                    description: "Dashboard full-stack para monitorear y gestionar recursos de infraestructura en múltiples nubes (AWS/GCP) para clientes.",
                    role: "Desarrollador Full Stack",
                    results: "Centralización de métricas de rendimiento y costos. API RESTful para la integración de datos y frontend en React para visualización.",
                    tags: ["React", "Flask", "Python", "AWS", "GCP", "PostgreSQL"]
                }
            ],

            services: [
                {
                    title: "Desarrollo Backend & APIs",
                    description: "Construcción de APIs RESTful robustas y escalables en Python (Flask), optimizadas con Redis y Celery para alto rendimiento."
                },
                {
                    title: "Arquitectura y Migración Cloud",
                    description: "Diseño de soluciones en GCP y AWS, especializándome en la migración de sistemas legacy (.NET/C++) a arquitecturas modernas en la nube."
                },
                {
                    title: "Soluciones de IA y Datos",
                    description: "Implementación de soluciones de IA (Vertex AI, RAG) y diseño de orquestaciones de datos complejas para procesamiento a gran escala."
                }
            ],

            experience: [
                {
                    title: "Software Engineer (Backend & Cloud)",
                    company: "Equifax (vía 23people)",
                    location: "Santiago, Chile",
                    period: "Enero 2025 – Presente",
                    points: [
                        "Lidero la refactorización y migración de servicios legacy (.NET/SQL/C++) a una arquitectura moderna en Python y PostgreSQL en GCP.",
                        "Diseño e implemento orquestaciones de datos complejas para el procesamiento y consumo de grandes volúmenes de información.",
                        "Automatizo procesos de ingesta y transformación de datos, mejorando la eficiencia y fiabilidad de los servicios."
                    ]
                },
                {
                    title: "Desarrollador Full Stack (Cloud)",
                    company: "Multicloud-X",
                    location: "Santiago, Chile",
                    period: "Marzo 2024 – Diciembre 2024",
                    points: [
                        "Desarrollé e integré APIs RESTful y asíncronas para aplicaciones cloud-native en AWS y GCP.",
                        "Gestioné la infraestructura de bases de datos SQL (PostgreSQL) y NoSQL (MongoDB).",
                        "Impartí webinars técnicos sobre \"Automatización con RPA en GCP\" y \"Casos de uso de Copilot\"."
                    ]
                }
            ],

            education: {
                title: "Ingeniería en Computación e Informática",
                institution: "Universidad Andrés Bello | Santiago, Chile",
                period: "Finaliza en 2025"
            },
            
            certifications: [
                "<strong>Cloud Digital Leader</strong> | Google Cloud (2024)",
                "<strong>Technical Accredited</strong> | Amazon Web Services (2024)"
            ],

            // Contenido de la sección CV (resumen)
            cvSummary: {
                summary: `Ingeniero de Software con +1 año de experiencia, especializado en desarrollo Backend con Python y arquitectura Cloud (GCP/AWS). Experto en la migración de sistemas legacy...`,
                exp1_title: "<strong>Software Engineer (Backend & Cloud)</strong> | Equifax (vía 23people) | Ene 2025 – Presente",
                exp1_list: [
                    "Lideré la refactorización y migración de servicios legacy (.NET/SQL/C++)..."
                ],
                exp2_title: "<strong>Desarrollador Full Stack (Cloud)</strong> | Multicloud-X | Mar 2024 – Dic 2024",
                exp2_list: [
                    "Desarrollé e integré APIs RESTful y asíncronas..."
                ],
                proj1_title: "<strong>QuickFlow (Asistente Virtual con IA)</strong> | Desarrollador Líder | Abr 2025 – Oct 2025",
                proj1_list: [
                    "Dirigí el desarrollo de un chatbot empresarial en GCP utilizando Gemini (Vertex AI)..."
                ],
                education: "<strong>Ingeniería en Computación e Informática</strong> | Universidad Andrés Bello (Finaliza 2025)",
                languages: "<strong>Idiomas:</strong> Español (Nativo), Inglés (Nivel C2)"
            },

            // Contenido de la Carta de Presentación
            coverLetter: {
                date: "20 de octubre de 2025",
                greeting: "Estimado Equipo de Contratación,",
                p1: `Le escribo para expresar mi gran interés en posiciones de Software Engineer. Como Ingeniero de Software especializado en desarrollo Backend y arquitectura Cloud (GCP/AWS), mi experiencia en la migración de servicios legacy y el diseño de soluciones de datos escalables se alinea perfectamente con los desafíos de roles en su empresa.`,
                p2: `En mi rol actual como Software Engineer en Equifax, lidero la refactorización de servicios .NET y C++ a arquitecturas modernas en Python, diseñando e implementando orquestaciones de datos críticas. Mi capacidad para optimizar sistemas quedó demostrada en mi proyecto "QuickFlow", un asistente virtual basado en Gemini (Vertex AI) y RAG, donde desarrollé una API RESTful en Python capaz de gestionar altas cargas de consultas mediante Redis y Celery.`,
                p3: `Mi objetivo es aplicar mi experiencia técnica en Python, GCP y Vertex AI para construir y optimizar sistemas de backend que impulsen soluciones innovadoras. La oportunidad de contribuir a su equipo y resolver desafíos de datos a gran escala es exactamente el siguiente paso que busco en mi carrera.`,
                p4: `Estoy convencido de que mi perfil técnico y mi capacidad de autoaprendizaje me permitirían aportar un valor significativo.`,
                signoff: "Atentamente,",
                name: "Erick Riquelme Yáñez"
            }
        };

        // ===================================================================
        // LÓGICA DE RENDERIZADO                                             
        // No es necesario editar debajo de esta línea.                   
        // ===================================================================
        document.addEventListener('DOMContentLoaded', () => {
            const config = portfolioConfig;

            // --- 1. Aplicar Colores ---
            const colors = config.colors;
            Object.keys(colors).forEach(key => {
                document.documentElement.style.setProperty(`--color-${key.replace('_', '-')}`, colors[key]);
            });

            // --- 2. Poblar Contenido Estático y Perfil ---
            const profile = config.profile;
            // Nav
            document.getElementById('nav-name').textContent = profile.name;
            // Hero
            document.getElementById('hero-name').textContent = profile.name;
            document.getElementById('hero-title').textContent = profile.title;
            document.getElementById('hero-email').href = `mailto:${profile.email}`;
            document.getElementById('hero-email-text').textContent = profile.email;
            document.getElementById('hero-linkedin').href = profile.linkedin;
            document.getElementById('hero-github').href = profile.github;
            document.getElementById('hero-image').src = profile.imageUrl;
            // Perfil
            document.getElementById('profile-summary').innerHTML = config.profileSummary;
            // Educación
            document.getElementById('education-title').textContent = config.education.title;
            document.getElementById('education-institution').textContent = config.education.institution;
            document.getElementById('education-period').textContent = config.education.period;
            // Footer
            document.getElementById('footer-email').href = `mailto:${profile.email}`;
            document.getElementById('footer-email').textContent = profile.email;
            document.getElementById('footer-linkedin').href = profile.linkedin;
            document.getElementById('footer-github').href = profile.github;
            document.getElementById('footer-copyright').textContent = `© ${profile.copyrightYear} ${profile.name}. Todos los derechos reservados.`;

            // --- 3. Poblar Habilidades ---
            const skillsContainer = document.getElementById('skills-container');
            skillsContainer.innerHTML = '';
            config.skills.forEach(skill => {
                const p = document.createElement('p');
                let skillsHTML = '';
                skill.list.split(',').forEach(s => {
                    skillsHTML += `<span class="skill">${s.trim()}</span>`;
                });
                p.innerHTML = `<strong class="text-white">${skill.category}:</strong> ${skillsHTML}`;
                skillsContainer.appendChild(p);
            });

            // --- 4. Poblar Proyectos ---
            const projectsContainer = document.getElementById('projects-container');
            projectsContainer.innerHTML = '';
            config.projects.forEach(project => {
                const card = document.createElement('div');
                card.className = 'card';
                const tagsHTML = project.tags.map(tag => `<span class="tech-tag">${tag}</span>`).join(' ');
                card.innerHTML = `
                    <h4 class="font-bold text-xl text-white mb-2">${project.title}</h4>
                    <p class="text-gray-400 mb-4">${project.description}</p>
                    <p class="mb-1 text-gray-300"><strong>Rol:</strong> ${project.role}</p>
                    <p class="mb-1 text-gray-300"><strong>Resultados:</strong> ${project.results}</p>
                    <div class="mt-4">${tagsHTML}</div>
                `;
                projectsContainer.appendChild(card);
            });

            // --- 5. Poblar Servicios ---
            const servicesContainer = document.getElementById('services-container');
            servicesContainer.innerHTML = '';
            config.services.forEach(service => {
                const card = document.createElement('div');
                card.className = 'card text-center';
                card.innerHTML = `
                    <h4 class="font-bold text-xl text-white mb-2">${service.title}</h4>
                    <p class="text-gray-400">${service.description}</p>
                `;
                servicesContainer.appendChild(card);
            });

            // --- 6. Poblar Experiencia ---
            const expContainer = document.getElementById('experience-container');
            expContainer.innerHTML = '';
            config.experience.forEach(exp => {
                const div = document.createElement('div');
                const pointsHTML = exp.points.map(point => `<li>${point}</li>`).join('');
                div.innerHTML = `
                    <h4 class="font-bold text-xl text-white">${exp.title}</h4>
                    <p class="font-semibold text-lg text-gray-300 mb-1">${exp.company} | ${exp.location}</p>
                    <p class="text-sm text-gray-500 mb-3">${exp.period}</p>
                    <ul class="list-disc list-inside text-gray-300 space-y-1">
                        ${pointsHTML}
                    </ul>
                `;
                expContainer.appendChild(div);
            });

            // --- 7. Poblar Certificaciones ---
            const certsList = document.getElementById('certs-list');
            certsList.innerHTML = '';
            config.certifications.forEach(cert => {
                const li = document.createElement('li');
                li.innerHTML = cert;
                certsList.appendChild(li);
            });

            // --- 8. Poblar CV Resumen ---
            const cv = config.cvSummary;
            document.getElementById('cv-name').textContent = profile.name;
            document.getElementById('cv-title').textContent = profile.title;
            document.getElementById('cv-summary').innerHTML = cv.summary;
            document.getElementById('cv-exp1-title').innerHTML = cv.exp1_title;
            document.getElementById('cv-exp1-list').innerHTML = cv.exp1_list.map(p => `<li>${p}</li>`).join('');
            document.getElementById('cv-exp2-title').innerHTML = cv.exp2_title;
            document.getElementById('cv-exp2-list').innerHTML = cv.exp2_list.map(p => `<li>${p}</li>`).join('');
            document.getElementById('cv-proj1-title').innerHTML = cv.proj1_title;
            document.getElementById('cv-proj1-list').innerHTML = cv.proj1_list.map(p => `<li>${p}</li>`).join('');
            document.getElementById('cv-edu').innerHTML = cv.education;
            document.getElementById('cv-lang').innerHTML = cv.languages;

            // --- 9. Poblar Carta de Presentación ---
            const letter = config.coverLetter;
            document.getElementById('letter-date').textContent = letter.date;
            document.getElementById('letter-greeting').textContent = letter.greeting;
            document.getElementById('letter-p1').innerHTML = letter.p1;
            document.getElementById('letter-p2').innerHTML = letter.p2;
            document.getElementById('letter-p3').innerHTML = letter.p3;
            document.getElementById('letter-p4').innerHTML = letter.p4;
            document.getElementById('letter-signoff').textContent = letter.signoff;
            document.getElementById('letter-name').textContent = letter.name;
            
            // --- 10. Lógica de Animación ---
            const animatedElements = document.querySelectorAll('.section-title, #profile-summary, .card, #experience-container > div, #cv .max-w-4xl, #carta .max-w-4xl');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('fade-in');
                        observer.unobserve(entry.target); // Anim
                    }
                });
            }, { 
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px' // Comienza la animación un poco antes de que esté 100% en vista
            });

            animatedElements.forEach(el => {
                observer.observe(el);
            });

        });
    </script>
</body>
</html>
