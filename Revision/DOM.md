<div class="gdoc-page">
          
  


  






<div class="gdoc-page__header flex flex-wrap
  
    justify-end
  
  hidden-mobile
  hidden" itemprop="breadcrumb">
  
  
</div>



  <article class="gdoc-markdown gdoc-markdown__align--left">
    <h1>DOM</h1>
    <div class="gdoc-page__anchorwrap">
    <h2 id="structure-dun-document-html">
        Structure d’un document HTML
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/dom/#structure-dun-document-html" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Structure d’un document HTML" aria-label="Anchor to: Structure d’un document HTML" href="#structure-dun-document-html">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Un document HTML se compose d’éléments organisés comme une hiérarchie ayant la forme d’une arbre inversé. Chaque noeud dans cet arbre correspond à un type d’élément HTML qui peut avoir plusieurs noeuds enfants et au maximum un parent. Seule la <em>racine</em> (le noeud <code>document</code>, au sommet de la hiérarchie) n’a pas de parent.</p>
<p>L’exemple suivant correspond à un <a class="gdoc-markdown__link" href="/420-211/exemple-dom.html">document HTML simple</a>:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<!DOCTYPE html>
<html>
    <head>
        <script src=&quot;lib.js&quot;></script>
        <title>Page perso</title>
    </head>
    <body>
        <h1>Bienvenue</h1>
        <div>Voici du texte</div>
        <a href=&quot;https://www.google.com&quot;>Voici un lien</a>
    </body>
</html>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="cp">&lt;!DOCTYPE html&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">head</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">script</span> <span class="na">src</span><span class="o">=</span><span class="s">"lib.js"</span><span class="p">&gt;&lt;/</span><span class="nt">script</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">title</span><span class="p">&gt;</span>Page perso<span class="p">&lt;/</span><span class="nt">title</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">head</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">body</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">h1</span><span class="p">&gt;</span>Bienvenue<span class="p">&lt;/</span><span class="nt">h1</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span><span class="p">&gt;</span>Voici du texte<span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">a</span> <span class="na">href</span><span class="o">=</span><span class="s">"https://www.google.com"</span><span class="p">&gt;</span>Voici un lien<span class="p">&lt;/</span><span class="nt">a</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">body</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span></code></pre></div><p>Ce qui correspond au modèle suivant:</p>
<p><img src="./Images/dom.svg" alt="dom"></p>
<div class="gdoc-page__anchorwrap">
    <h2 id="objet-document">
        Objet <code>document</code>
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/dom/#objet-document" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Objet document" aria-label="Anchor to: Objet document" href="#objet-document">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Javascript comprend un objet nommé <strong>document</strong> qui permet d’accéder aux informations du DOM, de modifier des valeurs d’attributs ou du texte, d’ajouter, de supprimer ou de déplacer des éléments HTML, etc.</p>
<p>L’objet <code>document</code> comprend plusieurs méthodes pour accéder aux éléments du DOM; Parmi celles-ci:</p>
<div class="gdoc-page__anchorwrap">
    <h3 id="getelementbyid">
        <code>getElementById()</code>
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/dom/#getelementbyid" class="gdoc-page__anchor clip flex align-center" title="Anchor to: getElementById()" aria-label="Anchor to: getElementById()" href="#getelementbyid">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h3>
</div>
<p>Retourne l’élément HTML dont l’attribut <code>id</code> correspond à la valeur passée.</p>
<div class="gdoc-page__anchorwrap">
    <h3 id="getelementbytagname">
        <code>getElementByTagName()</code>
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/dom/#getelementbytagname" class="gdoc-page__anchor clip flex align-center" title="Anchor to: getElementByTagName()" aria-label="Anchor to: getElementByTagName()" href="#getelementbytagname">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h3>
</div>
<p>Retourne une collection d’éléments HTML dont les noms correspondent à la valeur passée.</p>
<div class="gdoc-page__anchorwrap">
    <h3 id="getelementbyclassname">
        <code>getElementByClassName()</code>
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/dom/#getelementbyclassname" class="gdoc-page__anchor clip flex align-center" title="Anchor to: getElementByClassName()" aria-label="Anchor to: getElementByClassName()" href="#getelementbyclassname">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h3>
</div>
<p>Retourne une collection d’éléments HTML dont les attributs <code>class</code> correspondent à la valeur passée.</p>
<p>Par exemple pour le code HTML suivant:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<!DOCTYPE html>
<html>
    <body>
        <h1 class=&quot;titre&quot;>Titre</h1>
        <h2 class=&quot;titre&quot;>Sous-titre</h2>
        <div>
            <p id=&quot;par1&quot; class=&quot;parag&quot;>Premier paragraphe</p>
            <p id=&quot;par2&quot; class=&quot;parag&quot; >Deuxième paragraphe</p>
        </div>
    </body>
</html>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="cp">&lt;!DOCTYPE html&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">body</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">h1</span> <span class="na">class</span><span class="o">=</span><span class="s">"titre"</span><span class="p">&gt;</span>Titre<span class="p">&lt;/</span><span class="nt">h1</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">h2</span> <span class="na">class</span><span class="o">=</span><span class="s">"titre"</span><span class="p">&gt;</span>Sous-titre<span class="p">&lt;/</span><span class="nt">h2</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">p</span> <span class="na">id</span><span class="o">=</span><span class="s">"par1"</span> <span class="na">class</span><span class="o">=</span><span class="s">"parag"</span><span class="p">&gt;</span>Premier paragraphe<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">p</span> <span class="na">id</span><span class="o">=</span><span class="s">"par2"</span> <span class="na">class</span><span class="o">=</span><span class="s">"parag"</span> <span class="p">&gt;</span>Deuxième paragraphe<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">body</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span></code></pre></div><ul>
<li><code>getElementById("par1")</code> retourne l’élément <code>&lt;p&gt;</code> “Premier paragraphe”;</li>
<li><code>getElementsByTagName("p")</code> retourne tous les éléments <code>&lt;p&gt;</code>;</li>
<li><code>getElementsByClassName("titre")</code> retourne les éléments <code>&lt;h1&gt;</code> et <code>&lt;h2&gt;</code>.</li>
</ul>





<blockquote class="gdoc-hint note">
  <div class="gdoc-hint__title flex align-center"><i class="fa note" title="Attention"></i></div>
  <div class="gdoc-hint__text">Lorsque ces méthodes retournent plus d’un élément, ceux-ci font partie d’une collection et on doit utiliser une boucle pour accéder à chacun individuellement.</div>
</blockquote>

<div class="gdoc-page__anchorwrap">
    <h2 id="propriétés-des-éléments">
        Propriétés des éléments
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/dom/#propriétés-des-éléments" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Propriétés des éléments" aria-label="Anchor to: Propriétés des éléments" href="#propri%c3%a9t%c3%a9s-des-%c3%a9l%c3%a9ments">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Les éléments HTML contiennent d’innombrables propriétés et méthodes qu’on peut utiliser pour en modifier le contenu. Ici nous verrons les propriétés <code>innerHTML</code> et <code>style</code>.</p>
<blockquote>
<p>Pour la référence complète de l’objet <code>Element</code> du DOM: <a class="gdoc-markdown__link" href="https://www.w3schools.com/jsref/dom_obj_all.asp">https://www.w3schools.com/jsref/dom_obj_all.asp</a>.</p>
</blockquote>
<div class="gdoc-page__anchorwrap">
    <h3 id="innerhtml">
        <code>innerHTML</code>
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/dom/#innerhtml" class="gdoc-page__anchor clip flex align-center" title="Anchor to: innerHTML" aria-label="Anchor to: innerHTML" href="#innerhtml">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h3>
</div>
<p>Permet d’accéder le contenu HTML d’un élément ou de le modifier. Par exemple, pour le document HTML de l’exemple plus haut:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="let el = document.getElementById(&quot;par1&quot;);
el.innerHTML=&quot;Bonjour&quot;;" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="kd">let</span> <span class="nx">el</span> <span class="o">=</span> <span class="nb">document</span><span class="p">.</span><span class="nx">getElementById</span><span class="p">(</span><span class="s2">"par1"</span><span class="p">);</span>
</span></span><span class="line"><span class="cl"><span class="nx">el</span><span class="p">.</span><span class="nx">innerHTML</span><span class="o">=</span><span class="s2">"Bonjour"</span><span class="p">;</span>
</span></span></code></pre></div><p>Le texte “Premier paragraphe” sera remplacé par “Bonjour”.</p>
<p>Attention, le texte ainsi inséré est interprété comme du HTML. On peut ainsi modifier indirectement la structure du DOM; par exmeple:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="let elems = document.getElementsByClassName(&quot;parag&quot;);
for (let i=0;i<elems.length;i++) {
    elems[i].innerHTML=&quot;<h1>Bonjour</h1>&quot;;
}" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="kd">let</span> <span class="nx">elems</span> <span class="o">=</span> <span class="nb">document</span><span class="p">.</span><span class="nx">getElementsByClassName</span><span class="p">(</span><span class="s2">"parag"</span><span class="p">);</span>
</span></span><span class="line"><span class="cl"><span class="k">for</span> <span class="p">(</span><span class="kd">let</span> <span class="nx">i</span><span class="o">=</span><span class="mi">0</span><span class="p">;</span><span class="nx">i</span><span class="o">&lt;</span><span class="nx">elems</span><span class="p">.</span><span class="nx">length</span><span class="p">;</span><span class="nx">i</span><span class="o">++</span><span class="p">)</span> <span class="p">{</span>
</span></span><span class="line"><span class="cl">    <span class="nx">elems</span><span class="p">[</span><span class="nx">i</span><span class="p">].</span><span class="nx">innerHTML</span><span class="o">=</span><span class="s2">"&lt;h1&gt;Bonjour&lt;/h1&gt;"</span><span class="p">;</span>
</span></span><span class="line"><span class="cl"><span class="p">}</span>
</span></span></code></pre></div><p>Les deux éléments <code>&lt;p&gt;</code> contiendront chacun un élément H1 ayant le texte “Bonjour”.</p>
<div class="gdoc-page__anchorwrap">
    <h3 id="style">
        <code>style</code>
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/dom/#style" class="gdoc-page__anchor clip flex align-center" title="Anchor to: style" aria-label="Anchor to: style" href="#style">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h3>
</div>
<p>La propriété <strong>style</strong> permet de changer les attributs de style. Tous les styles qui peuvent être définis par l’attribut HTML “style” ou dans un fichier CSS sont accessibles par <em>javascript</em>. Les noms des styles sont légèrement différents cependant car ils suivent la nomenclature “camelCase”: par exemple, la propriété CSS <code>background-color</code> est appelée <code>backgroundColor</code> dans <em>javascript</em>.</p>
<p>Par exemple, pour mettre en gras le texte des paragraphes d’un document:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="let elems = document.getElementsByTagName(&quot;p&quot;);
for (let i=0;i<elems.length;i++) {
    elems[i].style.fontWeight=&quot;bold&quot;;
}" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="kd">let</span> <span class="nx">elems</span> <span class="o">=</span> <span class="nb">document</span><span class="p">.</span><span class="nx">getElementsByTagName</span><span class="p">(</span><span class="s2">"p"</span><span class="p">);</span>
</span></span><span class="line"><span class="cl"><span class="k">for</span> <span class="p">(</span><span class="kd">let</span> <span class="nx">i</span><span class="o">=</span><span class="mi">0</span><span class="p">;</span><span class="nx">i</span><span class="o">&lt;</span><span class="nx">elems</span><span class="p">.</span><span class="nx">length</span><span class="p">;</span><span class="nx">i</span><span class="o">++</span><span class="p">)</span> <span class="p">{</span>
</span></span><span class="line"><span class="cl">    <span class="nx">elems</span><span class="p">[</span><span class="nx">i</span><span class="p">].</span><span class="nx">style</span><span class="p">.</span><span class="nx">fontWeight</span><span class="o">=</span><span class="s2">"bold"</span><span class="p">;</span>
</span></span><span class="line"><span class="cl"><span class="p">}</span>
</span></span></code></pre></div><blockquote>
<p>Pour la référence complète des propriétés de style : <a class="gdoc-markdown__link" href="https://www.w3schools.com/jsref/dom_obj_style.asp">https://www.w3schools.com/jsref/dom_obj_style.asp</a></p>
</blockquote>

  </article>

