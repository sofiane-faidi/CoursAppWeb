<div class="gdoc-page">
          
  


  






<div class="gdoc-page__header flex flex-wrap
  
    justify-end
  
  hidden-mobile
  hidden" itemprop="breadcrumb">
  
  
</div>



  <article class="gdoc-markdown gdoc-markdown__align--left">
    <h1>Fonctions JS</h1>
    <div class="gdoc-page__anchorwrap">
    <h2 id="fonctions-nommées">
        Fonctions nommées
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/fonction-js/#fonctions-nommées" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Fonctions nommées" aria-label="Anchor to: Fonctions nommées" href="#fonctions-nomm%c3%a9es">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Un <em>programme</em> est un ensemble d’instructions qui permettent de faire un calcul ou d’effectuer une tâche. Les <em>fonctions</em> sont une structure de programmation qui permet de rendre le code plus réutilisable et d’en améliorer l’organisation.</p>
<p>Les fonctions peuvent avoir des <em><strong>paramètres</strong></em> et peuvent <em><strong>retourner des valeurs</strong></em>.</p>
<p>La <em><strong>définition</strong></em> d’une fonction est l’endroit où on décrit les instructions qu’elle doit exécuter.</p>
<p>Les <em><strong>appels de fonction</strong></em> sont les endroits où elle est utilisée.</p>
<p>La fonction suivante ne prend aucun paramètre et ne retourne aucune valeur:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="function somme() {  // Définition
    let tot = 10 + 30;
    console.log(&quot;la somme est:&quot;, tot);
}
somme();            // Appel" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="kd">function</span> <span class="nx">somme</span><span class="p">()</span> <span class="p">{</span>  <span class="c1">// Définition
</span></span></span><span class="line"><span class="cl"><span class="c1"></span>    <span class="kd">let</span> <span class="nx">tot</span> <span class="o">=</span> <span class="mi">10</span> <span class="o">+</span> <span class="mi">30</span><span class="p">;</span>
</span></span><span class="line"><span class="cl">    <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s2">"la somme est:"</span><span class="p">,</span> <span class="nx">tot</span><span class="p">);</span>
</span></span><span class="line"><span class="cl"><span class="p">}</span>
</span></span><span class="line"><span class="cl"><span class="nx">somme</span><span class="p">();</span>            <span class="c1">// Appel
</span></span></span></code></pre></div><p>La fonction suivante prend deux paramètres, affiche un message et ne retourne aucune valeur:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="function somme(a,b) {   // Définition
    let tot = a + b;
    console.log(&quot;la somme est:&quot;, tot);
}
somme(10,30);           // Appel" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="kd">function</span> <span class="nx">somme</span><span class="p">(</span><span class="nx">a</span><span class="p">,</span><span class="nx">b</span><span class="p">)</span> <span class="p">{</span>   <span class="c1">// Définition
</span></span></span><span class="line"><span class="cl"><span class="c1"></span>    <span class="kd">let</span> <span class="nx">tot</span> <span class="o">=</span> <span class="nx">a</span> <span class="o">+</span> <span class="nx">b</span><span class="p">;</span>
</span></span><span class="line"><span class="cl">    <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s2">"la somme est:"</span><span class="p">,</span> <span class="nx">tot</span><span class="p">);</span>
</span></span><span class="line"><span class="cl"><span class="p">}</span>
</span></span><span class="line"><span class="cl"><span class="nx">somme</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">30</span><span class="p">);</span>           <span class="c1">// Appel
</span></span></span></code></pre></div><p>La fonction suivante prend deux paramètres et retourne leur somme (avec le mot clé <code>return</code>), sans l’afficher:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="function somme(a,b) {   // Définition
    return a + b;
}
console.log(&quot;la somme est:&quot;, somme(10,30)); // Appel" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="kd">function</span> <span class="nx">somme</span><span class="p">(</span><span class="nx">a</span><span class="p">,</span><span class="nx">b</span><span class="p">)</span> <span class="p">{</span>   <span class="c1">// Définition
</span></span></span><span class="line"><span class="cl"><span class="c1"></span>    <span class="k">return</span> <span class="nx">a</span> <span class="o">+</span> <span class="nx">b</span><span class="p">;</span>
</span></span><span class="line"><span class="cl"><span class="p">}</span>
</span></span><span class="line"><span class="cl"><span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s2">"la somme est:"</span><span class="p">,</span> <span class="nx">somme</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">30</span><span class="p">));</span> <span class="c1">// Appel
</span></span></span></code></pre></div><div class="gdoc-page__anchorwrap">
    <h3 id="fonctions-anonymes">
        Fonctions anonymes
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/fonction-js/#fonctions-anonymes" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Fonctions anonymes" aria-label="Anchor to: Fonctions anonymes" href="#fonctions-anonymes">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h3>
</div>
<p>En <em>javascript</em>, les fonctions peuvent être <em><strong>anonymes</strong></em>, c’est-à-dire qu’on ne leur donne pas de nom au moment de leur définition. Ceci permet de les affecter à des variables, de les passer à d’autres fonctions, etc. On les définit comme suit:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="const auto = function () {  
    return &quot;vroum&quot;;
}" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="kr">const</span> <span class="nx">auto</span> <span class="o">=</span> <span class="kd">function</span> <span class="p">()</span> <span class="p">{</span>  
</span></span><span class="line"><span class="cl">    <span class="k">return</span> <span class="s2">"vroum"</span><span class="p">;</span>
</span></span><span class="line"><span class="cl"><span class="p">}</span>
</span></span></code></pre></div>




<blockquote class="gdoc-hint caution">
  <div class="gdoc-hint__title flex align-center"><i class="fa caution" title="Attention"></i></div>
  <div class="gdoc-hint__text">Dans l’exemple précédent <code>auto</code> n’est pas le nom d’une fonction: c’est le nom d’une variable qui contient une définition de fonction. On pourrait croire que c’est la même chose (et dans bien des cas, les deux sont utilisées de la même manière), mais dans certaines circonstances la différence est importante.</div>
</blockquote>

<p>Tout comme les fonctions ordinaires, les fonctions anonymes peuvent prendre des paramètres. Par exemple la fonction <code>somme()</code>, définie plus haut, ressemble à ceci si on en fait une fonction anonyme:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="const somme = function (a,b) {  
    return a + b;
}" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="kr">const</span> <span class="nx">somme</span> <span class="o">=</span> <span class="kd">function</span> <span class="p">(</span><span class="nx">a</span><span class="p">,</span><span class="nx">b</span><span class="p">)</span> <span class="p">{</span>  
</span></span><span class="line"><span class="cl">    <span class="k">return</span> <span class="nx">a</span> <span class="o">+</span> <span class="nx">b</span><span class="p">;</span>
</span></span><span class="line"><span class="cl"><span class="p">}</span>
</span></span></code></pre></div>




<blockquote class="gdoc-hint tip">
  <div class="gdoc-hint__title flex align-center"><i class="fa tip" title="Important"></i></div>
  <div class="gdoc-hint__text">Pour appeler une fonction anonyme, il faut invoquer la variable qui la contient suivie de parenthèses (et de ses arguments s’il y en a) par exemple: <code>auto()</code>, <code>somme(10,40)</code>. L’appel d’une fonction anonyme est donc semblable à l’appel d’une fonction ordinaire.</div>
</blockquote>


  </article>


