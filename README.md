<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Descubrí tu tipo de inteligencia 🧠</title>
  <style>
    :root{
      --bg: #f5efe6; /* beige claro */
      --card: #ffffff;
      --text: #1f2937;
      --muted: #586069;
      --accent: #2b6cb0;
      --radius: 12px;
      font-family: "Inter", "Segoe UI", Roboto, Arial, sans-serif;
    }
    html,body{height:100%;}
    body{
      margin:0;
      background:var(--bg);
      color:var(--text);
      -webkit-font-smoothing:antialiased;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:24px;
    }
    .wrap{
      width:100%;
      max-width:900px;
      background:transparent;
    }
    .card{
      background:var(--card);
      border-radius:var(--radius);
      box-shadow: 0 8px 30px rgba(15,23,42,0.08);
      padding:20px;
      margin-bottom:14px;
    }
    header{
      text-align:center;
      margin-bottom:12px;
    }
    h1{
      margin:0;
      font-size:20px;
      letter-spacing:-0.2px;
    }
    p.lead{
      margin:6px 0 0 0;
      color:var(--muted);
      font-size:14px;
    }

    form{
      display:flex;
      flex-direction:column;
      gap:14px;
    }

    .q{
      display:block;
      padding:12px;
      border-radius:10px;
      border:1px solid rgba(15,23,42,0.06);
    }
    .q h3{
      margin:0 0 8px 0;
      font-size:15px;
    }
    .options{
      display:grid;
      grid-template-columns:repeat(2,1fr);
      gap:8px;
    }
    .opt{
      display:flex;
      gap:10px;
      align-items:center;
      padding:8px 10px;
      border-radius:8px;
      cursor:pointer;
      user-select:none;
      border:1px solid rgba(15,23,42,0.04);
      transition:all .12s;
      background:#fafafa;
    }
    .opt input{display:none;}
    .opt:hover{transform:translateY(-2px);}
    .opt.selected{
      background: linear-gradient(90deg, rgba(43,108,176,0.08), rgba(43,108,176,0.03));
      border-color: rgba(43,108,176,0.25);
      box-shadow: 0 4px 12px rgba(43,108,176,0.06);
    }
    .letter{
      min-width:30px;
      height:30px;
      border-radius:8px;
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:600;
      border:1px solid rgba(15,23,42,0.06);
      background:#fff;
    }
    .text{
      font-size:14px;
      color:var(--text);
    }

    .result{
      display:none;
      text-align:center;
      padding:18px;
      border-radius:10px;
    }
    .result.show{display:block;}
    .result h2{
      margin:0;
      font-size:18px;
    }
    .result p{color:var(--muted); margin:10px 0 0 0;}
    .actions{
      display:flex;
      justify-content:center;
      gap:12px;
      margin-top:14px;
    }
    button{
      border:0;
      padding:10px 14px;
      border-radius:10px;
      cursor:pointer;
      font-weight:600;
      background:var(--accent);
      color:white;
      box-shadow:0 6px 18px rgba(43,108,176,0.12);
    }
    button.ghost{
      background:transparent;
      color:var(--accent);
      border:1px solid rgba(43,108,176,0.12);
      box-shadow:none;
    }

    footer{
      margin-top:10px;
      text-align:center;
      color:var(--muted);
      font-size:13px;
    }

    /* Responsive */
    @media (max-width:560px){
      .options{grid-template-columns:1fr;}
      h1{font-size:18px;}
    }
  </style>
</head>
<body>
  <div class="wrap">
    <div class="card" role="region" aria-labelledby="title">
      <header>
        <h1 id="title">Descubrí tu tipo de inteligencia 🧠</h1>
        <p class="lead">Hacé este test rápido y descubrí cuál de las 8 inteligencias dominás más.</p>
      </header>

      <form id="quiz" autocomplete="off" novalidate>
        <!-- Question 1 -->
        <div class="q" data-q="1">
          <h3>1. En tu tiempo libre, preferís:</h3>
          <div class="options">
            <label class="opt"><span class="letter">A</span><span class="text">Escuchar música o tocar un instrumento.</span>
              <input type="radio" name="q1" value="A">
            </label>
            <label class="opt"><span class="letter">B</span><span class="text">Resolver rompecabezas o acertijos.</span>
              <input type="radio" name="q1" value="B">
            </label>
            <label class="opt"><span class="letter">C</span><span class="text">Charlar con amigos o ayudar a alguien.</span>
              <input type="radio" name="q1" value="C">
            </label>
            <label class="opt"><span class="letter">D</span><span class="text">Dibujar, sacar fotos o decorar cosas.</span>
              <input type="radio" name="q1" value="D">
            </label>
            <label class="opt"><span class="letter">E</span><span class="text">Hacer deporte o mover el cuerpo.</span>
              <input type="radio" name="q1" value="E">
            </label>
            <label class="opt"><span class="letter">F</span><span class="text">Estar en la naturaleza o cuidar animales.</span>
              <input type="radio" name="q1" value="F">
            </label>
            <label class="opt"><span class="letter">G</span><span class="text">Pensar en tus emociones o escribir un diario.</span>
              <input type="radio" name="q1" value="G">
            </label>
          </div>
        </div>

        <!-- Question 2 -->
        <div class="q" data-q="2">
          <h3>2. En la escuela o trabajo, se te da mejor:</h3>
          <div class="options">
            <label class="opt"><span class="letter">A</span><span class="text">Música o arte.</span>
              <input type="radio" name="q2" value="A">
            </label>
            <label class="opt"><span class="letter">B</span><span class="text">Matemática o lógica.</span>
              <input type="radio" name="q2" value="B">
            </label>
            <label class="opt"><span class="letter">C</span><span class="text">Lengua, teatro o debate.</span>
              <input type="radio" name="q2" value="C">
            </label>
            <label class="opt"><span class="letter">D</span><span class="text">Plástica o diseño.</span>
              <input type="radio" name="q2" value="D">
            </label>
            <label class="opt"><span class="letter">E</span><span class="text">Educación física o danza.</span>
              <input type="radio" name="q2" value="E">
            </label>
            <label class="opt"><span class="letter">F</span><span class="text">Ciencias naturales o ecología.</span>
              <input type="radio" name="q2" value="F">
            </label>
            <label class="opt"><span class="letter">G</span><span class="text">Psicología, filosofía o escritura personal.</span>
              <input type="radio" name="q2" value="G">
            </label>
          </div>
        </div>

        <!-- Question 3 -->
        <div class="q" data-q="3">
          <h3>3. Cuando aprendés algo nuevo, preferís:</h3>
          <div class="options">
            <label class="opt"><span class="letter">A</span><span class="text">Escucharlo o cantarlo como una canción.</span>
              <input type="radio" name="q3" value="A">
            </label>
            <label class="opt"><span class="letter">B</span><span class="text">Analizarlo paso a paso y entender el porqué.</span>
              <input type="radio" name="q3" value="B">
            </label>
            <label class="opt"><span class="letter">C</span><span class="text">Explicarlo o practicarlo con otras personas.</span>
              <input type="radio" name="q3" value="C">
            </label>
            <label class="opt"><span class="letter">D</span><span class="text">Dibujarlo o imaginarlo con imágenes.</span>
              <input type="radio" name="q3" value="D">
            </label>
            <label class="opt"><span class="letter">E</span><span class="text">Hacerlo en la práctica, moviéndote.</span>
              <input type="radio" name="q3" value="E">
            </label>
            <label class="opt"><span class="letter">F</span><span class="text">Relacionarlo con la naturaleza o animales.</span>
              <input type="radio" name="q3" value="F">
            </label>
            <label class="opt"><span class="letter">G</span><span class="text">Pensar cómo te hace sentir o qué significa para vos.</span>
              <input type="radio" name="q3" value="G">
            </label>
          </div>
        </div>

        <!-- Question 4 -->
        <div class="q" data-q="4">
          <h3>4. Te sentís más cómodo cuando:</h3>
          <div class="options">
            <label class="opt"><span class="letter">A</span><span class="text">Hay música de fondo.</span>
              <input type="radio" name="q4" value="A">
            </label>
            <label class="opt"><span class="letter">B</span><span class="text">Todo está ordenado y tiene lógica.</span>
              <input type="radio" name="q4" value="B">
            </label>
            <label class="opt"><span class="letter">C</span><span class="text">Trabajás en grupo o con amigos.</span>
              <input type="radio" name="q4" value="C">
            </label>
            <label class="opt"><span class="letter">D</span><span class="text">Podés usar colores, imágenes o gráficos.</span>
              <input type="radio" name="q4" value="D">
            </label>
            <label class="opt"><span class="letter">E</span><span class="text">Te movés o hacés algo activo.</span>
              <input type="radio" name="q4" value="E">
            </label>
            <label class="opt"><span class="letter">F</span><span class="text">Estás al aire libre o cerca de la naturaleza.</span>
              <input type="radio" name="q4" value="F">
            </label>
            <label class="opt"><span class="letter">G</span><span class="text">Tenés tiempo a solas para pensar o reflexionar.</span>
              <input type="radio" name="q4" value="G">
            </label>
          </div>
        </div>

        <!-- Question 5 -->
        <div class="q" data-q="5">
          <h3>5. Si pudieras participar en un concurso, elegirías:</h3>
          <div class="options">
            <label class="opt"><span class="letter">A</span><span class="text">Cantar o tocar un instrumento.</span>
              <input type="radio" name="q5" value="A">
            </label>
            <label class="opt"><span class="letter">B</span><span class="text">Resolver un acertijo o desafío mental.</span>
              <input type="radio" name="q5" value="B">
            </label>
            <label class="opt"><span class="letter">C</span><span class="text">Liderar un grupo o hacer una entrevista.</span>
              <input type="radio" name="q5" value="C">
            </label>
            <label class="opt"><span class="letter">D</span><span class="text">Crear una maqueta, dibujo o video.</span>
              <input type="radio" name="q5" value="D">
            </label>
            <label class="opt"><span class="letter">E</span><span class="text">Competir en un deporte o coreografía.</span>
              <input type="radio" name="q5" value="E">
            </label>
            <label class="opt"><span class="letter">F</span><span class="text">Hacer un experimento o cuidar una planta.</span>
              <input type="radio" name="q5" value="F">
            </label>
            <label class="opt"><span class="letter">G</span><span class="text">Escribir algo inspirador o dar un mensaje positivo.</span>
              <input type="radio" name="q5" value="G">
            </label>
          </div>
        </div>
      </form>

      <div id="result" class="card result" aria-live="polite">
        <h2 id="resultTitle"></h2>
        <p id="resultDesc"></p>
        <div class="actions">
          <button id="tryAgain" class="ghost">Volver a intentarlo</button>
        </div>
      </div>

      <footer>
        <small>Test rápido • Ideal para la expo</small>
      </footer>
    </div>
  </div>

  <script>
    (function(){
      const form = document.getElementById('quiz');
      const resultBox = document.getElementById('result');
      const titleEl = document.getElementById('resultTitle');
      const descEl = document.getElementById('resultDesc');
      const tryAgain = document.getElementById('tryAgain');

      // mapping letter -> intelligence
      const mapping = {
        A: { key:'musical', emoji:'🎵', name:'Inteligencia Musical', desc: 'Tenés oído sensible, amás la música y te expresás a través de los sonidos.' },
        B: { key:'logical', emoji:'🧩', name:'Inteligencia Lógico-Matemática', desc: 'Sos analítico/a, te gusta resolver problemas y encontrar soluciones lógicas.' },
        C: { key:'interpersonal', emoji:'💬', name:'Inteligencia Interpersonal', desc: 'Entendés a los demás, sabés comunicarte y trabajar en equipo.' },
        D: { key:'spatial', emoji:'🎨', name:'Inteligencia Visual-Espacial', desc: 'Tenés mucha imaginación y te guiás por imágenes, colores y diseño.' },
        E: { key:'kinesthetic', emoji:'🏃', name:'Inteligencia Corporal-Kinestésica', desc: 'Aprendés moviéndote, usando tu cuerpo o haciendo cosas prácticas.' },
        F: { key:'naturalist', emoji:'🌿', name:'Inteligencia Naturalista', desc: 'Te encanta la naturaleza, los animales y cuidar el entorno.' },
        G: { key:'intrapersonal', emoji:'💭', name:'Inteligencia Intrapersonal', desc: 'Sos reflexivo/a, te conocés bien y entendés tus emociones.' }
      };

      // helper to compute result
      function computeResult(){
        const data = new FormData(form);
        const counts = {A:0,B:0,C:0,D:0,E:0,F:0,G:0};
        // check all 5 q's present
        for(let i=1;i<=5;i++){
          const val = data.get('q'+i);
          if(!val) return null; // not finished
          if(counts.hasOwnProperty(val)) counts[val]++;
        }
        // find max
        let maxLetter = 'A', maxVal = -1;
        for(const l of Object.keys(counts)){
          if(counts[l] > maxVal){
            maxVal = counts[l];
            maxLetter = l;
          }
        }
        return mapping[maxLetter];
      }

      // UI: mark selected options
      document.querySelectorAll('.options').forEach(opts=>{
        opts.addEventListener('click', e=>{
          const label = e.target.closest('label.opt');
          if(!label) return;
          const input = label.querySelector('input[type="radio"]');
          if(!input) return;
          input.checked = true;
          // mark selection style
          const container = label.closest('.options');
          container.querySelectorAll('label.opt').forEach(l=>l.classList.remove('selected'));
          label.classList.add('selected');

          // check if all answered -> compute
          const r = computeResult();
          if(r){
            showResult(r);
          }
        });
      });

      function showResult(data){
        titleEl.textContent = `${data.emoji} ${data.name}`;
        descEl.textContent = data.desc;
        resultBox.classList.add('show');
        // scroll result into view on small screens
        setTimeout(()=> resultBox.scrollIntoView({behavior:'smooth', block:'center'}), 200);
      }

      tryAgain.addEventListener('click', ()=>{
        // reset form
        form.reset();
        document.querySelectorAll('label.opt').forEach(l=>l.classList.remove('selected'));
        resultBox.classList.remove('show');
        // scroll top
        window.scrollTo({top:0, behavior:'smooth'});
      });

      // Accessibility: if user used keyboard to change radio, detect change
      form.addEventListener('change', () => {
        const r = computeResult();
        if(r) showResult(r);
      });

    })();
  </script>
</body>
</html>
