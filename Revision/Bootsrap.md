<div class="gdoc-page">
          
  


  






<div class="gdoc-page__header flex flex-wrap
  
    justify-end
  
  hidden-mobile
  hidden" itemprop="breadcrumb">
  
  
</div>



  <article class="gdoc-markdown gdoc-markdown__align--left">
    <h1>Bootstrap</h1>
    <p><em>Bootstrap</em> est un ensemble prédéfini de classes CSS qui facilite l’organisation des éléments d’une page. Avec <em>Bootstrap</em>, on peut créer facilement les composantes habituelles d’une page web moderne (boutons, menus, caroussels d’images, etc.), modifier les éléments typographiques (titres, couleurs, listes et citations) et surtout réorganiser dynamiquement les éléments d’une page selon la taille de l’écran.</p>
<p>Pour utiliser <em>Bootstrap</em> dans un document HTML, il faut lui ajouter les références suivantes dans l’entête (la balise <code>&lt;head&gt;</code>):</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<link href=&quot;https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css&quot; rel=&quot;stylesheet&quot;>
<script src=&quot;https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js&quot;></script>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">link</span> <span class="na">href</span><span class="o">=</span><span class="s">"https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css"</span> <span class="na">rel</span><span class="o">=</span><span class="s">"stylesheet"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">script</span> <span class="na">src</span><span class="o">=</span><span class="s">"https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"</span><span class="p">&gt;&lt;/</span><span class="nt">script</span><span class="p">&gt;</span>
</span></span></code></pre></div><div class="gdoc-page__anchorwrap">
    <h1 id="structure">
        Structure
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#structure" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Structure" aria-label="Anchor to: Structure" href="#structure">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h1>
</div>
<p>La structure d’une page en <em>Bootstrap</em> comprend trois niveaux:</p>
<ul>
<li>Conteneurs</li>
<li>Rangées</li>
<li>Colonnes</li>
</ul>
<p>Les conteneurs contiennent les rangées et les rangées contiennent les colonnes. Ces composantes correspondent à des classes CSS qu’on donne à des éléments <code>&lt;div&gt;</code> dans le DOM. Par exemple, pour le code HTML suivant:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<div class=&quot;container&quot;>
    <div class=&quot;row&quot;>
        <div class=&quot;col&quot;></div>
        <div class=&quot;col&quot;></div>
    </div>
    <div class=&quot;row&quot;>
        <div class=&quot;col&quot;></div>
        <div class=&quot;col&quot;></div>
        <div class=&quot;col&quot;></div>
    </div>
    <div class=&quot;row&quot;>
        <div class=&quot;col&quot;></div>
    </div>
</div>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"container"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"row"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"row"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"row"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span></code></pre></div><p>on aura la disposition suivante:</p>
<p><img src="../Images/struct.svg" alt="struct"></p>
<div class="gdoc-page__anchorwrap">
    <h2 id="container">
        <code>container</code>
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#container" class="gdoc-page__anchor clip flex align-center" title="Anchor to: container" aria-label="Anchor to: container" href="#container">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>C’est l’élément de base. Identifié par <code>&lt;div class="container"&gt;</code>.</p>
<ul>
<li>La classe <code>container</code> a une marge et une largeur inférieure à celle de l’écran</li>
<li>La classe <code>container-fluid</code> occupe la pleine largeur de l’écran.</li>
</ul>
<p>En général, on utilise un seul conteneur par page.</p>
<div class="gdoc-page__anchorwrap">
    <h2 id="row">
        <code>row</code>
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#row" class="gdoc-page__anchor clip flex align-center" title="Anchor to: row" aria-label="Anchor to: row" href="#row">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Les rangées permettent de diviser l’espace d’un conteneur du haut en bas. Elles sont identifiées par <code>&lt;div class="row"&gt;</code>. On peut en mettre autant qu’on veut dans un même conteneur.</p>
<p>La taille verticale d’une rangée est déterminée par son contenu.</p>
<div class="gdoc-page__anchorwrap">
    <h2 id="column">
        <code>column</code>
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#column" class="gdoc-page__anchor clip flex align-center" title="Anchor to: column" aria-label="Anchor to: column" href="#column">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Les colonnes divisent de gauche à droite l’espace d’une rangée. Elles sont identifiées par <code>&lt;div class="col"&gt;</code>.</p>
<p>La taille horizontale d’une colonne est déterminée par le nombre total de colonnes de la rangée: donc si une rangée contient 2 colonnes, chacune occupe la moitié de l’espace; si elle en contient 3, chacune occupe un tiers de l’espace; etc.</p>
<p>Il est cependant possible de spécifier des proportions différentes.</p>
<div class="gdoc-page__anchorwrap">
    <h2 id="la-grille-bootstrap">
        La grille bootstrap
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#la-grille-bootstrap" class="gdoc-page__anchor clip flex align-center" title="Anchor to: La grille bootstrap" aria-label="Anchor to: La grille bootstrap" href="#la-grille-bootstrap">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Le modèle de <em>bootstrap</em> est basé sur une grille de 12 colonnes: si on veut contrôler nous-mêmes la taille des colonnes il faut ajouter un suffixe numérique d’une valeur de 1 à 12 à la classe <strong>col</strong>. Ce nombre correspond à la largeur (sur 12) que la colonne occupe dans la page. Par exemple:</p>
<ul>
<li><code>col-1</code> a une largeur de 1/12 de la page</li>
<li><code>col-4</code> a une largeur de 4/12 (donc un tiers) de la page</li>
<li><code>col-9</code> a une largeur de 3/4 de la page</li>
<li>etc.</li>
</ul>
<p>Lorsqu’on ne spécifie pas de taille, toute la largeur est occupée; ainsi <code>col-12</code> a le même effet que <code>col</code>.</p>
<p>Donc, pour la structure suivante:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<div class=&quot;container&quot;>
    <div class=&quot;row&quot;>
        <div class=&quot;col-8&quot;></div>
        <div class=&quot;col-4&quot;></div>
    </div>
    <div class=&quot;row&quot;>
        <div class=&quot;col-3&quot;></div>
        <div class=&quot;col-6&quot;></div>
        <div class=&quot;col-3&quot;></div>
    </div>
</div>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"container"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"row"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-8"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-4"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"row"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-3"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-6"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-3"</span><span class="p">&gt;&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>    
</span></span></code></pre></div><p>on aura la disposition suivante:</p>
<p><img src="../Images/grid1.png" alt="grille"></p>
<p><a class="gdoc-markdown__link" href="/420-211/ressources/exemple-grille.html">(exemple)</a></p>
<div class="gdoc-page__anchorwrap">
    <h1 id="transitions">
        Transitions
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#transitions" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Transitions" aria-label="Anchor to: Transitions" href="#transitions">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h1>
</div>
<p>Afin de permettre au contenu d’une page de bien s’adapter aux différentes tailles des écrans (PC, tablette, cellulaire…), <em>bootstrap</em> définit 6 tailles d’écran possibles:</p>
<ul>
<li><code>xs</code>: <em>extra-small</em></li>
<li><code>sm</code>: <em>small</em></li>
<li><code>md</code>: <em>medium</em></li>
<li><code>lg</code>: <em>large</em></li>
<li><code>xl</code>: <em>extra-large</em></li>
<li><code>xxl</code>: <em>extra-extra-large</em></li>
</ul>
<p>Lorsque l’écran est redimensionné, on peut utiliser ces tailles avec les classes <strong>col</strong> pour ajuster la taille des colonnes. Par exemple <code>class="col-md-6"</code> signifie qu’on a une largeur de 6 pour les tailles <em>medium</em> et plus; les tailles inférieures, puisqu’elles ne sont pas spécifiées, occupent la pleine largeur.</p>
<p>Dans l’exemple suivant, 3 <strong>div</strong> ont la classe <code>col-sm-4</code>; donc, chaque <strong>div</strong> occupe un tiers (4/12) de l’espace pour la taille d’écran “small” et les tailles plus grandes:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<div class=&quot;container&quot;>
    <div class=&quot;row&quot;>
        <div class=&quot;col-sm-4&quot;>
            <h2>col-sm-4</h2>
            <p>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.</p>
        </div>
        <div class=&quot;col-sm-4&quot;>
            <h2>col-sm-4</h2>
            <p>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.</p>
        </div>
        <div class=&quot;col-sm-4&quot;>
            <h2>col-sm-4</h2>
            <p>Cras porttitor ullamcorper dam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.</p>
        </div>
    </div>
</div>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"container"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"row"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-sm-4"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">h2</span><span class="p">&gt;</span>col-sm-4<span class="p">&lt;/</span><span class="nt">h2</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-sm-4"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">h2</span><span class="p">&gt;</span>col-sm-4<span class="p">&lt;/</span><span class="nt">h2</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-sm-4"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">h2</span><span class="p">&gt;</span>col-sm-4<span class="p">&lt;/</span><span class="nt">h2</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>Cras porttitor ullamcorper dam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>    
</span></span></code></pre></div><p><a class="gdoc-markdown__link" href="/420-211/ressources/exemple-responsive.html">(exemple)</a></p>





<blockquote class="gdoc-hint note">
  <div class="gdoc-hint__title flex align-center"><i class="fa note" title="Note"></i></div>
  <div class="gdoc-hint__text">Puisque <code>xs</code> est la taille minimale, il n’y a pas de transition entre elle et une taille plus petite. Il est donc inutile de définir une largeur de colonne comme <code>col-xs-3</code>, puisque cela est équivalent à <code>col-3</code>.</div>
</blockquote>

<p>On peut définir plus d’une transition pour un même élément. Par exemple une rangée peut contenir 4 éléments pour les grandes tailles, 2 rangées de 2 éléments pour les tailles moyennes et 4 rangées de 1 élément pour les petites tailles. Pour ce fait il suffit de donner deux classes pour un même élément. L’exemple suivant illustre ceci:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<div class=&quot;container&quot;>
    <div class=&quot;row&quot;>
        <div class=&quot;col-sm-6 col-lg-3&quot;>
            <h2>Titre 1</h2>
            <p>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.</p>
        </div>
        <div class=&quot;col-sm-6 col-lg-3&quot;>
            <h2>Titre 2</h2>
            <p>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.</p>
        </div>
        <div class=&quot;col-sm-6 col-lg-3&quot;>
            <h2>Titre 3</h2>
            <p>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.</p>
        </div>
        <div class=&quot;col-sm-6 col-lg-3&quot;>
            <h2>Titre 4</h2>
            <p>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.</p>
        </div>
    </div>
</div>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"container"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"row"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-sm-6 col-lg-3"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">h2</span><span class="p">&gt;</span>Titre 1<span class="p">&lt;/</span><span class="nt">h2</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-sm-6 col-lg-3"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">h2</span><span class="p">&gt;</span>Titre 2<span class="p">&lt;/</span><span class="nt">h2</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-sm-6 col-lg-3"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">h2</span><span class="p">&gt;</span>Titre 3<span class="p">&lt;/</span><span class="nt">h2</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"col-sm-6 col-lg-3"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">h2</span><span class="p">&gt;</span>Titre 4<span class="p">&lt;/</span><span class="nt">h2</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">            <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>Cras porttitor ullamcorper diam et vulputate. Praesent non mauris nec sem consequat auctor nec vel leo. Aenean pulvinar enim ac iaculis convallis.<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>    
</span></span></code></pre></div><p><a class="gdoc-markdown__link" href="/420-211/ressources/exemple-responsive2.html">(exemple)</a></p>
<div class="gdoc-page__anchorwrap">
    <h1 id="composantes">
        Composantes
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#composantes" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Composantes" aria-label="Anchor to: Composantes" href="#composantes">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h1>
</div>
<p>Dans cette section nous allons voir quelques exemples des composantes et éléments de style offerts par <em>Bootstrap</em>. La liste est très courte; l’objectif ici est simplement de se faire une idée générale de la manière dont on peut utiliser les éléments de style de ce cadriciel. Au fil de la session, nous aurons l’occasion de voir d’autres éléments.</p>
<p>Pour plus de détails sur les composantes <em>Bootstrap</em>, vous pouvez vous référer à la documentation technique (<a class="gdoc-markdown__link" href="https://getbootstrap.com/docs/5.0/getting-started/introduction/">https://getbootstrap.com/docs/5.0/getting-started/introduction/</a>)</p>
<div class="gdoc-page__anchorwrap">
    <h2 id="images">
        Images
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#images" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Images" aria-label="Anchor to: Images" href="#images">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<ul>
<li>Classe: <code>img-fluid</code></li>
<li>Élément: <code>&lt;img&gt;</code></li>
</ul>
<p>Lorsqu’on l’ajoute à un élément <code>&lt;img&gt;</code>, la classe <code>img-fluid</code> a pour effet de redimensionner automatiquement l’image afin qu’elle soit toujours de la taille de l’élément qui la contient.</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<img class=&quot;img-fluid&quot; src=&quot;test.png&quot; />" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">img</span> <span class="na">class</span><span class="o">=</span><span class="s">"img-fluid"</span> <span class="na">src</span><span class="o">=</span><span class="s">"test.png"</span> <span class="p">/&gt;</span>
</span></span></code></pre></div><div class="gdoc-page__anchorwrap">
    <h2 id="boutons">
        Boutons
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#boutons" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Boutons" aria-label="Anchor to: Boutons" href="#boutons">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<ul>
<li>Classe principale: <code>btn</code></li>
<li>Classes de style: <code>btn-lg</code>, <code>btn-sm</code>, <code>btn-primary</code>, <code>btn-secondary</code>, etc.</li>
<li>Éléments: <code>&lt;button&gt;</code>, <code>&lt;a&gt;</code></li>
</ul>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<button type=&quot;button&quot; class=&quot;btn btn-primary&quot;>Bouton &quot;button&quot;</button>
<a type=&quot;button&quot; class=&quot;btn btn-primary&quot; href=&quot;#&quot;>Bouton &quot;a&quot;</a>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">button</span> <span class="na">type</span><span class="o">=</span><span class="s">"button"</span> <span class="na">class</span><span class="o">=</span><span class="s">"btn btn-primary"</span><span class="p">&gt;</span>Bouton "button"<span class="p">&lt;/</span><span class="nt">button</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">a</span> <span class="na">type</span><span class="o">=</span><span class="s">"button"</span> <span class="na">class</span><span class="o">=</span><span class="s">"btn btn-primary"</span> <span class="na">href</span><span class="o">=</span><span class="s">"#"</span><span class="p">&gt;</span>Bouton "a"<span class="p">&lt;/</span><span class="nt">a</span><span class="p">&gt;</span>
</span></span></code></pre></div><p>Tous les boutons doivent avoir la classe <code>btn</code>; ensuite, selon le style qu’on veut leur donner on peut attribuer des classes pour leur taille (<code>btn-lg</code>, <code>btn-sm</code>) ou pour leur couleur (<code>btn-primary</code>, <code>btn-secondary</code>).</p>
<p>La classe <code>active</code> accentue la couleur du bouton.</p>
<p>La classe <code>disabled</code> désactive le bouton. Ceci a pour effet d’atténuer sa couleur et de rendre le clic impossible.</p>
<div class="gdoc-page__anchorwrap">
    <h2 id="menu">
        Menu
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#menu" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Menu" aria-label="Anchor to: Menu" href="#menu">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<ul>
<li>Classes: <code>nav</code>, <code>nav-item</code>, <code>nav-link</code></li>
<li>Éléments: <code>&lt;ul&gt;</code>, <code>&lt;li&gt;</code></li>
</ul>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<ul class=&quot;nav&quot;>
    <li class=&quot;nav-item&quot;>
        <a class=&quot;nav-link&quot; href=&quot;#&quot;>Item 1</a> 
    </li>
    <li class=&quot;nav-item&quot;>
        <a class=&quot;nav-link&quot; href=&quot;#&quot;>Item 2</a> 
    </li>
</ul>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">ul</span> <span class="na">class</span><span class="o">=</span><span class="s">"nav"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">li</span> <span class="na">class</span><span class="o">=</span><span class="s">"nav-item"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">a</span> <span class="na">class</span><span class="o">=</span><span class="s">"nav-link"</span> <span class="na">href</span><span class="o">=</span><span class="s">"#"</span><span class="p">&gt;</span>Item 1<span class="p">&lt;/</span><span class="nt">a</span><span class="p">&gt;</span> 
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">li</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">li</span> <span class="na">class</span><span class="o">=</span><span class="s">"nav-item"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">a</span> <span class="na">class</span><span class="o">=</span><span class="s">"nav-link"</span> <span class="na">href</span><span class="o">=</span><span class="s">"#"</span><span class="p">&gt;</span>Item 2<span class="p">&lt;/</span><span class="nt">a</span><span class="p">&gt;</span> 
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">li</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">ul</span><span class="p">&gt;</span>
</span></span></code></pre></div><p>L’élément parent d’un menu est <code>&lt;ul&gt;</code> et on doit lui donner la classe <code>nav</code>; chaque item du menu correspond à un sous-élément <code>&lt;li&gt;</code> qui doit avoir la classe <code>nav-item</code> et le lien <code>&lt;a&gt;</code> vers la page de destination doit avoir la classe <code>nav-link</code>.</p>
<p>Comme pour les boutons, la classe <code>active</code> accentue la couleur de l’item du menu, et la classe <code>disabled</code> désactive l’item du menu.</p>





<blockquote class="gdoc-hint tip">
  <div class="gdoc-hint__title flex align-center"><i class="fa tip" title="Remarque"></i></div>
  <div class="gdoc-hint__text">Ces classes permettent de créer des menus simples. La classe <code>navbar</code>, plus flexible mais plus complexe, donne accès à des fonctionnalités de menu plus élaborées.</div>
</blockquote>

<div class="gdoc-page__anchorwrap">
    <h2 id="cards">
        Cards
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/R%C3%A9vision/bootstrap/#cards" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Cards" aria-label="Anchor to: Cards" href="#cards">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<ul>
<li>Classes principales: <code>card</code>, <code>card-body</code>, <code>card-title</code>, <code>card-text</code></li>
<li>Classes secondaires: <code>card-header</code>, <code>card-footer</code>, <code>card-img-top</code>, etc.</li>
</ul>
<p>Les “cartes” sont un type de conteneur simple qui permet de regrouper dans un petit espace des informations de toutes sortes. Elles ont une bordure par défaut et peuvent contenir des images, des titres, du texte, des boutons, etc.</p>
<p>Le format minimal de carte (qui contient uniquement du texte) contient deux <code>&lt;div&gt;</code> imbriqués; le parent a la classe <code>card</code> et l’enfant a la classe <code>card-body</code>:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<div class=&quot;card&quot;>
    <div class=&quot;card-body&quot;>
        <p>Texte de la carte</p>
    </div>
</div>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"card"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"card-body"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>Texte de la carte<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span></code></pre></div><p>Pour ajouter une image à la carte, on utilise un élément <code>&lt;img&gt;</code>. Celui-ci doit avoir <code>card</code> comme parent immédiat.</p>
<p>Le code suivant montre un exemple de carte plus complexe qui comprend une entête et un pied, une image, un titre et du contenu texte:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<div class=&quot;card&quot;>
    <div class=&quot;card-header p-3&quot;>
        Entête
    </div>
    <img src=&quot;patate.png&quot; />
    <div class=&quot;card-body text-center&quot;>
        <h5 class=&quot;card-title&quot;>Titre de la carte</h5>
        <p class=&quot;card-text&quot;>Texte de la carte</p>
    </div>
    <div class=&quot;card-footer&quot;>
        Pied
    </div>
</div>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"card"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"card-header p-3"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        Entête
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">img</span> <span class="na">src</span><span class="o">=</span><span class="s">"patate.png"</span> <span class="p">/&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"card-body text-center"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">h5</span> <span class="na">class</span><span class="o">=</span><span class="s">"card-title"</span><span class="p">&gt;</span>Titre de la carte<span class="p">&lt;/</span><span class="nt">h5</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">p</span> <span class="na">class</span><span class="o">=</span><span class="s">"card-text"</span><span class="p">&gt;</span>Texte de la carte<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">class</span><span class="o">=</span><span class="s">"card-footer"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        Pied
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span></code></pre></div><p><a class="gdoc-markdown__link" href="/420-211/ressources/card1.html">(exemple)</a></p>

  </article>

