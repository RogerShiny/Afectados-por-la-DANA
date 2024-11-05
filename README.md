<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Afectados por la DANA</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background: #333;
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }

        header nav ul {
            list-style: none;
            padding: 0;
        }

        header nav ul li {
            display: inline;
            margin: 0 15px;
        }

        header nav ul li a {
            color: #fff;
            text-decoration: none;
        }

        header nav ul li a.active {
            color: yellow; /* Solo el texto activo en amarillo */
        }

        section {
            margin: 20px;
            padding: 20px;
            background: #fff;
            border-radius: 5px;
        }

        textarea {
            width: 100%;
            height: 100px;
            margin-bottom: 10px;
        }

        button {
            padding: 10px;
            background: #333;
            color: #fff;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background: #555;
        }
    </style>
</head>
<body>
    <header>
        <h1 id="titulo">Afectados por la DANA</h1>
        <nav>
            <ul>
                <li><a href="#" id="linkInicio" onclick="mostrarSeccion('inicio', this)">Inicio</a></li>
                <li><a href="#" id="linkQueEsDana" onclick="mostrarSeccion('queEsDana', this)">¿Qué es una DANA?</a></li>
                <li><a href="#" id="linkExperiencias" onclick="mostrarSeccion('experiencias', this)">Experiencias</a></li>
                <li><a href="#" id="linkAyuda" onclick="mostrarSeccion('ayuda', this)">Ayuda</a></li>
                <li><a href="#" id="linkVictimas" onclick="mostrarSeccion('victimas', this)">Víctimas y desaparecidos</a></li>
                <li><a href="#" id="linkNoticias" onclick="mostrarSeccion('noticias', this)">Últimas Noticias</a></li>
                <li><a href="#" id="linkOpiniones" onclick="mostrarSeccion('opiniones', this)">Opiniones</a></li>
            </ul>
        </nav>
        <div>
            <label for="idioma">Seleccionar idioma:</label>
            <select id="language-selector" onchange="cambiarIdioma()">
                <option value="es">Español</option>
                <option value="ca">Català</option>
            </select>
        </div>
    </header>

    <main>
        <section id="inicio" class="active">
            <h2 id="bienvenida">Bienvenido a Afectados por la DANA</h2>
            <p id="introduccion">Este foro está dedicado a ofrecer un espacio de encuentro, apoyo y solidaridad para las personas que se han visto afectadas por la DANA (Depresión Aislada en Niveles Altos), que, con su poder devastador, ha ocasionado inundaciones, desplazamientos forzosos, grandes daños materiales en varias regiones y, lo más gélido, muchísimas pérdidas de vidas humanas y animales. Aquí, tanto las víctimas como los testigos de la tragedia pueden compartir sus historias, ofrecer ayuda a quienes lo necesiten y, juntos, tratar de superar las consecuencias de estos desastres naturales. Además, este foro pretende ser una plataforma de información actualizada sobre las últimas noticias relacionadas con las DANA, los esfuerzos de rescate, y las medidas que se deben tomar para protegerse ante estos fenómenos climáticos.</p>
        </section>

        <section id="queEsDana">
            <h2 id="tituloQueEsDana">¿Qué es una DANA?</h2>
            <p id="descripcionQueEsDana">Una DANA (Depresión Aislada en Niveles Altos) es un fenómeno meteorológico caracterizado por la formación de una masa de aire frío aislada de la corriente en chorro, lo que provoca un enfriamiento brusco de la atmósfera en una zona determinada, generando tormentas violentas, lluvias torrenciales y vientos intensos. Este fenómeno meteorológico se da especialmente en las estaciones de otoño y primavera y puede causar graves inundaciones, desbordamientos de ríos y pérdidas materiales significativas. Las DANA son impredecibles, y su impacto puede ser catastrófico en zonas urbanas y rurales.</p>
            <h3>Actuación política y críticas</h3>
            <p id="actuacionPolitica">En los últimos años, la gestión política ante los efectos de las DANA ha sido duramente criticada. Los afectados por los fenómenos meteorológicos denuncian la falta de previsión, la lentitud en las ayudas y la insuficiencia de medidas preventivas. En varios casos, la respuesta del gobierno local y nacional ha sido percibida como inadecuada, especialmente durante las primeras horas del desastre, cuando se requería una acción rápida para salvar vidas y minimizar los daños.</p>
            <h3>Víctimas y Desaparecidos</h3>
            <p id="victimasDana">La reciente DANA, ocurrida en el mes de octubre de 2024, ha dejado un saldo trágico de víctimas mortales y desaparecidos. Las lluvias torrenciales y las inundaciones han arrasado con numerosas viviendas, y muchas personas han perdido la vida o siguen desaparecidas, a pesar de los esfuerzos de los equipos de rescate. En total, se han reportado más de 243 muertes confirmadas, el gobierno autonómico no ha querido confirmar la cifra de desaparecidos, pero algunas fuentes no oficiales apuntat que al menos hay 1500 personas aún desaparecidas, mientras se continúan las labores de búsqueda y rescate. A su vez, los servicios médicos y las organizaciones humanitarias están trabajando incansablemente para atender a los afectados, proporcionando refugio y asistencia alimentaria.</p>
        </section>

        <section id="experiencias">
            <h2 id="tituloExperiencias">Experiencias</h2>
            <textarea id="experiencia" placeholder="Comparte tu experiencia aquí..."></textarea>
            <button id="boton-compartir" onclick="compartirExperiencia()">Compartir</button>
            <div id="listaExperiencias"></div>
        </section>

        <section id="ayuda">
            <h2 id="tituloAyuda">Ayuda</h2>
            <textarea id="ayudaNecesaria" placeholder="¿Qué necesitas o qué ofreces?"></textarea>
            <button id="boton-ayuda" onclick="compartirAyuda()">Ofrecer/Pedir Ayuda</button>
            <div id="listaAyuda"></div>
        </section>

        <section id="victimas">
            <h2 id="tituloVictimas">Víctimas y Desaparecidos</h2>
            <h3>Si eres víctima de la DANA:</h3>
            <p id="victimas-info1">Si eres una víctima directa de la DANA, es importante que sigas los siguientes pasos para protegerte y acceder a la ayuda necesaria:</p>
            <ul id="victimas-lista1">
                <li>Busca refugio en lugares seguros y alejados de las zonas inundadas o peligrosas.</li>
                <li>Contacta con los servicios de emergencia o ayuda humanitaria para recibir asistencia inmediata.</li>
                <li>Informa a tus familiares y amigos sobre tu ubicación y estado.</li>
                <li>Accede a servicios de atención psicológica si experimentas estrés o trauma debido al desastre.</li>
            </ul>
            <h3>Si buscas a personas desaparecidas:</h3>
            <p id="victimas-info2">Si tienes familiares, amigos o conocidos desaparecidos, puedes hacer lo siguiente para tratar de encontrarlos:</p>
            <ul id="victimas-lista2">
                <li>Publica sus detalles (nombre, foto, últimos lugares conocidos) en redes sociales, grupos comunitarios y plataformas de búsqueda de personas.</li>
                <li>Contacta con las autoridades locales y presenta una denuncia para que se inicien las labores de búsqueda.</li>
                <li>Visita los refugios y centros de atención de emergencias en las zonas afectadas para obtener más información sobre posibles supervivientes.</li>
                <li>Mantente informado de las actualizaciones a través de los medios de comunicación y redes sociales.</li>
            </ul>
        </section>

        <section id="noticias">
            <h2 id="tituloNoticias">Últimas Noticias</h2>
            <p>Aquí se mostrarán las últimas noticias relacionadas con los efectos de la DANA y los esfuerzos de rescate. Mantente al tanto de los reportes más recientes y las recomendaciones de las autoridades locales.</p>
            <div id="noticiasLista">
                <h3>Noticia 1: Puente apunta al jueves de la próxima semana para recuperar la alta velocidad entre Madrid y València</h3>
               
                <h3>Noticia 2: El Jimbee donará la taquilla del partido ante el Manzanares a los afectados por la dana</h3>
                
            </div>
        </section>

        <section id="opiniones">
            <h2 id="tituloOpiniones">Opiniones</h2>
            <textarea id="opinion" placeholder="Comparte tu opinión..."></textarea>
            <button id="boton-compartir" onclick="compartirOpinion()">Compartir Opinión</button>
            <div id="listaOpiniones"></div>
        </section>
    </main>

    <script>
        const textos = {
            es: {
                titulo: "Afectados por la DANA",
                bienvenida: "Bienvenido al Foro sobre Afectados por la DANA",
                introduccion: "Este foro está dedicado a ofrecer un espacio de encuentro, apoyo y solidaridad para las personas que se han visto afectadas por fenómenos meteorológicos como la DANA (Depresión Aislada en Niveles Altos), que, con su poder devastador, ha ocasionado inundaciones, desplazamientos forzosos, pérdida de vidas y grandes daños materiales en varias regiones. Aquí, tanto las víctimas como los testigos de la tragedia pueden compartir sus historias, ofrecer ayuda a quienes lo necesiten y, juntos, tratar de superar las consecuencias de estos desastres naturales. Además, este foro pretende ser una plataforma de información actualizada sobre las últimas noticias relacionadas con las DANA, los esfuerzos de rescate, y las medidas que se deben tomar para protegerse ante estos fenómenos climáticos.",
                tituloExperiencias: "Experiencias",
                botonCompartir: "Compartir",
                tituloAyuda: "Ayuda",
                botonAyuda: "Ofrecer/Pedir Ayuda",
                tituloVictimas: "Víctimas y Desaparecidos",
                victimasInfo1: "Si eres víctima de la DANA:",
                victimasLista1: [
                    "Busca refugio seguro y contacta a los servicios de emergencia si es necesario.",
                    "Informa a tus familiares y amigos sobre tu estado.",
                    "Accede a servicios de atención psicológica si lo necesitas."
                ],
                victimasInfo2: "Si buscas a personas desaparecidas:",
                victimasLista2: [
                    "Publica su información en redes sociales y grupos comunitarios.",
                    "Contacta a las autoridades locales y presenta una denuncia.",
                    "Visita refugios y centros de ayuda para obtener información."
                ],
                tituloNoticias: "Últimas Noticias",
                noticias: [
                    "Noticia 1: Rescate en zonas afectadas por la DANA",
                    "Noticia 2: Aumento de víctimas mortales"
                ]
            },
            ca: {
                titulo: "Fòrum DANA",
                bienvenida: "Benvingut al Fòrum DANA",
                introduccion: "Aquest fòrum està dedicat a oferir un espai de trobada, suport i solidaritat per a les persones que s'han vist afectades per fenòmens meteorològics com la DANA (Depressió Aïllada en Nivells Alts), que, amb el seu poder devastador, ha ocasionat inundacions, desplaçaments forçosos, pèrdues de vides i grans danys materials a diverses regions. Aquí, tant les víctimes com els testimonis de la tragèdia poden compartir les seves històries, oferir ajuda a qui ho necessiti i, junts, tractar de superar les conseqüències d'aquests desastres naturals. A més, aquest fòrum pretén ser una plataforma d'informació actualitzada sobre les últimes notícies relacionades amb les DANAs, els esforços de rescat, i les mesures que s'han de prendre per protegir-se davant d'aquests fenòmens climàtics.",
                tituloExperiencias: "Experiències",
                botonCompartir: "Compartir",
                tituloAyuda: "Ajuda",
                botonAyuda: "Oferir/Pedir Ajuda",
                tituloVictimas: "Víctimes i Desapareguts",
                victimasInfo1: "Si ets víctima de la DANA:",
                victimasLista1: [
                    "Busca refugi segur i contacta amb els serveis d'emergència si és necessari.",
                    "Informa els teus familiars i amics sobre el teu estat.",
                    "Accedeix a serveis d'atenció psicològica si ho necessites."
                ],
                victimasInfo2: "Si busques persones desaparegudes:",
                victimasLista2: [
                    "Publica la seva informació a les xarxes socials i grups comunitaris.",
                    "Contacta amb les autoritats locals i presenta una denúncia.",
                    "Visita refugis i centres d'ajuda per obtenir informació."
                ],
                tituloNoticias: "Últimes Notícies",
                noticias: [
                    "Notícia 1: Rescat a zones afectades per la DANA",
                    "Notícia 2: Augment de víctimes mortals"
                ]
            }
        };

        function cambiarIdioma() {
            const idiomaSeleccionado = document.getElementById('language-selector').value;
            document.getElementById('titulo').textContent = textos[idiomaSeleccionado].titulo;
            document.getElementById('bienvenida').textContent = textos[idiomaSeleccionado].bienvenida;
            document.getElementById('introduccion').textContent = textos[idiomaSeleccionado].introduccion;
            document.getElementById('titulo-experiencias').textContent = textos[idiomaSeleccionado].tituloExperiencias;
            document.getElementById('boton-compartir').textContent = textos[idiomaSeleccionado].botonCompartir;
            document.getElementById('titulo-ayuda').textContent = textos[idiomaSeleccionado].tituloAyuda;
            document.getElementById('boton-ayuda').textContent = textos[idiomaSeleccionado].botonAyuda;
            document.getElementById('titulo-victimas').textContent = textos[idiomaSeleccionado].tituloVictimas;
            document.getElementById('victimas-info1').textContent = textos[idiomaSeleccionado].victimasInfo1;
            document.getElementById('victimas-info2').textContent = textos[idiomaSeleccionado].victimasInfo2;
            document.getElementById('titulo-noticias').textContent = textos[idiomaSeleccionado].tituloNoticias;
            
            const lista1 = document.getElementById('victimas-lista1');
            lista1.innerHTML = '';
            textos[idiomaSeleccionado].victimasLista1.forEach(item => {
                const li = document.createElement('li');
                li.textContent = item;
                lista1.appendChild(li);
            });

            const lista2 = document.getElementById('victimas-lista2');
            lista2.innerHTML = '';
            textos[idiomaSeleccionado].victimasLista2.forEach(item => {
                const li = document.createElement('li');
                li.textContent = item;
                lista2.appendChild(li);
            });

            const noticiasLista = document.getElementById('noticiasLista');
            noticiasLista.innerHTML = '';
            textos[idiomaSeleccionado].noticias.forEach(noticia => {
                const h3 = document.createElement('h3');
                h3.textContent = noticia;
                noticiasLista.appendChild(h3);
            });
        }

        function mostrarSeccion(seccion, link) {
            const secciones = document.querySelectorAll('main > section');
            secciones.forEach(s => {
                s.style.display = 'none'; // Ocultar todas las secciones
            });
            document.getElementById(seccion).style.display = 'block'; // Mostrar la sección seleccionada
            
            // Cambiar color del enlace activo
            const enlaces = document.querySelectorAll('header nav ul li a');
            enlaces.forEach(e => e.classList.remove('active'));
            link.classList.add('active'); // Resaltar el enlace activo
        }

        function compartirExperiencia() {
            const experiencia = document.getElementById("experiencia").value;
            const lista = document.getElementById("listaExperiencias");
            lista.innerHTML += `<div class="comentario"><p>${experiencia}</p></div>`;
            document.getElementById("experiencia").value = "";
        }

        function compartirAyuda() {
            const ayuda = document.getElementById("ayudaNecesaria").value;
            const lista = document.getElementById("listaAyuda");
            lista.innerHTML += `<div class="comentario"><p>${ayuda}</p></div>`;
            document.getElementById("ayudaNecesaria").value = "";
        }

        function compartirOpinion() {
            const opinion = document.getElementById("opinion").value;
            const lista = document.getElementById("listaOpiniones");
            lista.innerHTML += `<div class="comentario"><p>${opinion}</p></div>`;
            document.getElementById("opinion").value = "";
        }

        window.onload = function() {
            mostrarSeccion('inicio', document.getElementById("linkInicio"));
        };
    </script>
</body>
</html>
