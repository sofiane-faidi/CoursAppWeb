<div class="gdoc-page">
          
  


  






<div class="gdoc-page__header flex flex-wrap
  
    justify-end
  
  hidden-mobile
  hidden" itemprop="breadcrumb">
  
  
</div>



  <article class="gdoc-markdown gdoc-markdown__align--left">
    <h1>CSS</h1>
    <p>Il est possible de modifier l’apparence des éléments d’une page directement dans le code HTML en utilisant les attributs de style. Par exemple, pour changer la couleur du texte d’un paragraphe:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<div>
    <p>Texte normal</p>
    <p style=&quot;color:red&quot;>Texte rouge</p>
    <p style=&quot;background-color:yellow&quot;>Arrière-plan jaune</p>
</div>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>Texte normal<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">p</span> <span class="na">style</span><span class="o">=</span><span class="s">"color:red"</span><span class="p">&gt;</span>Texte rouge<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">p</span> <span class="na">style</span><span class="o">=</span><span class="s">"background-color:yellow"</span><span class="p">&gt;</span>Arrière-plan jaune<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">div</span><span class="p">&gt;</span>
</span></span></code></pre></div><p>On recommande cependant de regrouper ces propriétés dans un fichier CSS: ceci permet de centraliser les éléments de style et de permettre plus facilement les modifications. Par exemple, si on souhaite que les citations dans un texte soient en italique, sans serif et de couleur grise, on pourra définir une classe nommée “citation” dans un fichier CSS et y spécifier ces propriétés typographiques, comme suit:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text=".citation {
    font-family: sans-serif;
    color: grey;
    font-style: italic;
}" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-css" data-lang="css"><span class="line"><span class="cl"><span class="p">.</span><span class="nc">citation</span> <span class="p">{</span>
</span></span><span class="line"><span class="cl">    <span class="k">font-family</span><span class="p">:</span> <span class="kc">sans-serif</span><span class="p">;</span>
</span></span><span class="line"><span class="cl">    <span class="k">color</span><span class="p">:</span> <span class="kc">grey</span><span class="p">;</span>
</span></span><span class="line"><span class="cl">    <span class="k">font-style</span><span class="p">:</span> <span class="kc">italic</span><span class="p">;</span>
</span></span><span class="line"><span class="cl"><span class="p">}</span>
</span></span></code></pre></div><p>Par la suite, on attribue la classe <code>citation</code> à l’élément HTML dont on veut modifier le style:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<p class=&quot;citation&quot;>Alea Jacta Est</p>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">p</span> <span class="na">class</span><span class="o">=</span><span class="s">"citation"</span><span class="p">&gt;</span>Alea Jacta Est<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span></code></pre></div><p>Pour que le navigateur puisse retrouver le fichier CSS où le style est défini, il faut y ajouter une référence dans le fichier HTML dans un élément <code>&lt;link&gt;</code>. En supposant que le fichier qui contient les styles se nomme <em>styles.css</em>, on aura donc le code HTML suivant:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="<!DOCTYPE html>
<html>
    <head>
        <link href=&quot;styles.css&quot; rel=&quot;stylesheet&quot;>
    </head>
    <body>
        <p class=&quot;citation&quot;>Alea Jacta Est</p>
        <p>- Jules César</p>
    </body>
</html>" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-html" data-lang="html"><span class="line"><span class="cl"><span class="cp">&lt;!DOCTYPE html&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">head</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">link</span> <span class="na">href</span><span class="o">=</span><span class="s">"styles.css"</span> <span class="na">rel</span><span class="o">=</span><span class="s">"stylesheet"</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">head</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;</span><span class="nt">body</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">p</span> <span class="na">class</span><span class="o">=</span><span class="s">"citation"</span><span class="p">&gt;</span>Alea Jacta Est<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">        <span class="p">&lt;</span><span class="nt">p</span><span class="p">&gt;</span>- Jules César<span class="p">&lt;/</span><span class="nt">p</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl">    <span class="p">&lt;/</span><span class="nt">body</span><span class="p">&gt;</span>
</span></span><span class="line"><span class="cl"><span class="p">&lt;/</span><span class="nt">html</span><span class="p">&gt;</span>
</span></span></code></pre></div><blockquote>
</blockquote>
<p>Une référence complète des propriétés CSS est disponible sur le site <a class="gdoc-markdown__link" href="https://www.w3schools.com/cssref/index.php">https://www.w3schools.com/cssref/index.php</a>.</p>

  </article>

