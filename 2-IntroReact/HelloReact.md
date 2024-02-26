<div class="gdoc-page">

<div class="gdoc-page__header flex flex-wrap
  
justify-end
hidden-mobile
hidden" itemprop="breadcrumb">
  
</div>

  <article class="gdoc-markdown gdoc-markdown__align--left">
    <h1>Hello React</h1>
    <div class="gdoc-page__anchorwrap">
    <h2 id="structure-des-fichiers-de-lapplication">
        Structure des fichiers de l’application
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/installation/Hello-React/#structure-des-fichiers-de-lapplication" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Structure des fichiers de l’application" aria-label="Anchor to: Structure des fichiers de l’application" href="#structure-des-fichiers-de-lapplication">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Le répertoire <code>/var/www</code>, où l’application a été créée, contient deux sous-répertoires:</p>
<ul>
<li><em>public</em>: contient la page elle-même et les fichiers qui peuvent faire l’objet d’une requête HTTP directe;</li>
<li><em>src</em>: contient les fichiers de ressources de l’application, tant les composantes javascript que les feuilles de style, images ou autres.</li>
</ul>
<div class="gdoc-page__anchorwrap">
    <h3 id="indexhtml">
        index.html
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/installation/Hello-React/#indexhtml" class="gdoc-page__anchor clip flex align-center" title="Anchor to: index.html" aria-label="Anchor to: index.html" href="#indexhtml">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h3>
</div>
<p>Le fichier qui contient le code HTML de l’application est <code>/var/www/public/index.html</code>. Ce fichier a la structure habituelle d’un fichier HTML (éléments HEAD, BODY, DIV etc.). Remarquez l’élément <code>&lt;div&gt;</code> ayant l’identifiant <em><strong>root</strong></em> : il constitue la racine de l’application; tout ce qu’il contient sera généré à partir de <em>React</em>.</p>
<div class="gdoc-page__anchorwrap">
    <h3 id="indexjs">
        index.js
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/installation/Hello-React/#indexjs" class="gdoc-page__anchor clip flex align-center" title="Anchor to: index.js" aria-label="Anchor to: index.js" href="#indexjs">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h3>
</div>
<p>Ce fichier est le point d’entrée de l’application. Il contient le code qui génère la page.</p>
<p>La première ligne met dans une variable (nommée <code>root</code>) l’élément <code>&lt;div&gt;</code> que nous avons vu dans le fichier <code>index.html</code>:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="const root = ReactDOM.createRoot(document.getElementById('root'));" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-js" data-lang="js"><span class="line"><span class="cl"><span class="kr">const</span> <span class="nx">root</span> <span class="o">=</span> <span class="nx">ReactDOM</span><span class="p">.</span><span class="nx">createRoot</span><span class="p">(</span><span class="nb">document</span><span class="p">.</span><span class="nx">getElementById</span><span class="p">(</span><span class="s1">'root'</span><span class="p">));</span>
</span></span></code></pre></div><p>Dans la deuxième ligne, on appelle la fonction <em>render()</em> avec (entre autres) l’élément <code>&lt;App /&gt;</code> comme paramètre:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-jsx" data-lang="jsx"><span class="line"><span class="cl"><span class="nx">root</span><span class="p">.</span><span class="nx">render</span><span class="p">(</span>
</span></span><span class="line"><span class="cl">  <span class="p">&lt;</span><span class="nt">React.StrictMode</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">App</span> <span class="p">/&gt;</span>
</span></span><span class="line"><span class="cl">  <span class="p">&lt;/</span><span class="nt">React.StrictMode</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">);</span>
</span></span></code></pre></div><p>Ceci a pour effet d’appeler la fonction <em>App()</em> du fichier <strong>App.js</strong>. C’est cette fonction qui contient le code HTML qui sera affiché dans la page.</p>
<div class="gdoc-page__anchorwrap">
    <h3 id="appjs">
        App.js
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/installation/Hello-React/#appjs" class="gdoc-page__anchor clip flex align-center" title="Anchor to: App.js" aria-label="Anchor to: App.js" href="#appjs">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h3>
</div>
<p>Avec React, les page HTML sont construites grâce à des appels de fonction: les valeurs retournées par les fonctions seront rattachées aux différents éléments du DOM dans la page.</p>
<p>La fonction <code>App()</code> retourne les éléments qui seront immédiatement rattachés au DIV racine:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="function App() {
  return (
    <div className=&quot;App&quot;>
      <header className=&quot;App-header&quot;>
        <img src={logo} className=&quot;App-logo&quot; alt=&quot;logo&quot; />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className=&quot;App-link&quot;
          href=&quot;https://reactjs.org&quot;
          target=&quot;_blank&quot;
          rel=&quot;noopener noreferrer&quot;
        >
          Learn React
        </a>
      </header>
    </div>
  );
}" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-jsx" data-lang="jsx"><span class="line"><span class="cl"><span class="kd">function</span> <span class="nx">App</span><span class="p">()</span> <span class="p">{</span>
</span></span><span class="line"><span class="cl">  <span class="k">return</span> <span class="p">(</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">div</span> <span class="na">className</span><span class="o">=</span><span class="s">"App"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">      <span class="p">&lt;</span><span class="nt">header</span> <span class="na">className</span><span class="o">=</span><span class="s">"App-header"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">img</span> <span class="na">src</span><span class="o">=</span><span class="p">{</span><span class="nx">logo</span><span class="p">}</span> <span class="na">className</span><span class="o">=</span><span class="s">"App-logo"</span> <span class="na">alt</span><span class="o">=</span><span class="s">"logo"</span> <span class="p">/&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">          <span class="nx">Edit</span> <span class="p">&lt;</span><span class="nt">code</span><span class="p">&gt;</span><span class="nx">src</span><span class="o">/</span><span class="nx">App</span><span class="p">.</span><span class="nx">js</span><span class="p">&lt;/</span><span class="nt">code</span><span class="p">&gt;</span> <span class="nx">and</span> <span class="nx">save</span> <span class="nx">to</span> <span class="nx">reload</span><span class="p">.</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">a</span>
</span></span><span class="line"><span class="cl">          <span class="na">className</span><span class="o">=</span><span class="s">"App-link"</span>
</span></span><span class="line"><span class="cl">          <span class="na">href</span><span class="o">=</span><span class="s">"https://reactjs.org"</span>
</span></span><span class="line"><span class="cl">          <span class="na">target</span><span class="o">=</span><span class="s">"_blank"</span>
</span></span><span class="line"><span class="cl">          <span class="na">rel</span><span class="o">=</span><span class="s">"noopener noreferrer"</span>
</span></span><span class="line"><span class="cl">        <span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">          <span class="nx">Learn</span> <span class="nx">React</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;/</span><span class="nt">a</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">      <span class="p">&lt;/</span><span class="nt">header</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">  <span class="p">);</span>
</span></span><span class="line"><span class="cl"><span class="p">}</span>
</span></span></code></pre></div><p>Quelques remarques au sujet de l’exemple précédent:</p>
<ul>
<li>Le code est similaire à du javascript</li>
<li>Le HTML retourné par la fonction n’est pas entre guillemets</li>
<li>L’attribut HTML <code>class</code> s’appelle ici <code>className</code></li>
</ul>
<p>Ces particulartiés viennent du fait que le langage utilisé dans cette page n’est pas exactement du javascript, mais une extension de javascript qu’on nomme <em><strong>JSX</strong></em>.</p>
<p>Une introduction à JSX sera faite dans la section suivante.</p>

  </article>

