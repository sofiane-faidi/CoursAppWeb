<div class="gdoc-page">



<div class="gdoc-page__header flex flex-wrap

justify-end

hidden-mobile
hidden" itemprop="breadcrumb">


</div>



<article class="gdoc-markdown gdoc-markdown__align--left">
<h1>Débogage JS</h1>
<div class="gdoc-page__anchorwrap">
<h2 id="exécution-de-scripts-js">
Exécution de scripts JS
<a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/outils/#exécution-de-scripts-js" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Exécution de scripts JS" aria-label="Anchor to: Exécution de scripts JS" href="#ex%c3%a9cution-de-scripts-js">
<svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
</a>
</h2>
</div>
<p>Javascript est un langage qui s’exécute dans le navigateur. Les programmes JS peuvent être directement inclus dans des balises HTML <code>&lt;script&gt;</code>, comme suit:</p>
<p><em><strong>index.html</strong></em></p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<!DOCTYPE html>
<html>
<head>
<script>
alert(&quot;ceci est un message&quot;);
</script>
</head>
<body></body>
</html>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="cp">&lt;!DOCTYPE html&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">head</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">script</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="nx">alert</span><span class="p">(</span><span class="s2">"ceci est un message"</span><span class="p">);</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">script</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">head</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">body</span><span class="p">&gt;&lt;/</span><span class="nt">body</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span></code></pre></div><p>ou encore inclus comme des fichiers qu’on désigne en utilisant l’attribut <code>src</code> de l’élément <code>&lt;script&gt;</code>:</p>
<p><em><strong>index.html</strong></em></p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<!DOCTYPE html>
<html>
<head>
<script src=&quot;monProgramme.js&quot;></script>
</head>
<body></body>
</html>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="cp">&lt;!DOCTYPE html&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">head</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">script</span> <span class="na">src</span><span class="o">=</span><span class="s">"monProgramme.js"</span><span class="p">&gt;&lt;/</span><span class="nt">script</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">head</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">body</span><span class="p">&gt;&lt;/</span><span class="nt">body</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span></code></pre></div><p><em><strong>monProgramme.js</strong></em></p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="alert(&quot;ceci est un message&quot;)" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="nx">alert</span><span class="p">(</span><span class="s2">"ceci est un message"</span><span class="p">)</span>
</span></span></code></pre></div><div class="gdoc-page__anchorwrap">
<h2 id="outils-de-développement">
Outils de développement
<a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/outils/#outils-de-développement" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Outils de développement" aria-label="Anchor to: Outils de développement" href="#outils-de-d%c3%a9veloppement">
<svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
</a>
</h2>
</div>
<p>Dans ce cours nous utiliserons les outils de développement de <em>Firefox</em>. Pour y accéder, faites <code>CTRL-Maj-I</code> dans le navigateur.</p>
<div class="gdoc-page__anchorwrap">
<h3 id="console">
Console
<a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/outils/#console" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Console" aria-label="Anchor to: Console" href="#console">
<svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
</a>
</h3>
</div>
<p>La console permet d’évaluer directement des expressions en JS ou encore d’afficher des messages à partir d’un programme.</p>
<p>Pour évaluer des expressions il suffit de les taper sur la ligne de commande :
<img src="../Images/console.png" alt="console"></p>
<p>Pour afficher des messages à partir d’un programme il faut utiliser <code>console.log()</code> dans le programme, comme ceci:</p>
<p><em><strong>monProgramme.js:</strong></em></p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="console.log(&quot;Message à la console&quot;);" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s2">"Message à la console"</span><span class="p">);</span>
</span></span></code></pre></div><p>Au chargement de la page (et donc, de l’exécution du script JS), on verra le message apparaître:
<img src="../Images/console-log.png" alt="console-log"></p>
<div class="gdoc-page__anchorwrap">
<h3 id="débogueur">
Débogueur
<a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/outils/#débogueur" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Débogueur" aria-label="Anchor to: Débogueur" href="#d%c3%a9bogueur">
<svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
</a>
</h3>
</div>
<p>Les outils de développement de Firefox incluent un débogueur; parmi ses fonctionnalités il y a les <em><strong>points d’arrêt</strong></em> qui permettent de suspendre le flot d’exécution du programme et d’y inspecter les valeurs des variables. Ceci est très utile pour de détecter la cause des erreurs qui apparaissent au moment de l’exécution.</p>
<p>Pour mettre en pause un programme lorsqu’il arrive à une instruction donnée, il suffit de cliquer sur la marge de la ligne correspondante, ce qui crée un point d’arrêt (représenté par un marqueur bleu). Lors du rechargement de la page, l’exécution sera suspendue à cet endroit et les valeurs des variables (ici, <code>i: 1</code> et <code>limite: 1000</code>) seront affichées:</p>
<p><img src="./Images/debug-bp.png" alt="debug-bp"></p>
<ul>
<li>La touche <strong>F10</strong> permet de passer à la prochaine instruction et ainsi de poursuivre ligne par ligne l’exécution du programme.</li>
<li>La touche <strong>F8</strong> continue l’exécution du programme. Évidemment, puisqu’ici le point d’arrêt est dans une boucle, le programme sera de nouveau suspendu à la prochaine itération.</li>
</ul>
<p>Il est possible d’associer des <em>conditions</em> aux points d’arrêt afin que le programme s’arrête seulement lorsque les variables ont une valeur spécifique. Pour ce faire il faut se placer sur la ligne du point d’arrêt et faire <code>CTRL-Maj-B</code>, puis définir la condition:</p>
<p><img src="../Images/debug-bpcond.png" alt="debug-bpcond"></p>
<p>Les points d’arrêt conditionnels sont identifiés par un marqueur <strong>jaune</strong>.</p>

</article>


