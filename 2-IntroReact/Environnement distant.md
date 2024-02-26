<div class="gdoc-page">
          
  


  






<div class="gdoc-page__header flex flex-wrap
  
    justify-end
  
  hidden-mobile
  hidden" itemprop="breadcrumb">
  
  
</div>



  <article class="gdoc-markdown gdoc-markdown__align--left">
    <h1>Environnement distant</h1>
    <p>Dans ce qui suit nous allons configurer VSCode pour qu’il se connecte directement sur un serveur distant utilisé pour le développement. C’est cette configuration qui est utilisée en classe.</p>
<div class="gdoc-page__anchorwrap">
    <h2 id="connexion-physique">
        Connexion physique
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/installation/EnvDistant/#connexion-physique" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Connexion physique" aria-label="Anchor to: Connexion physique" href="#connexion-physique">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Afin d’accéder à ce serveur de développement, vous devez vous connecter sur le réseau interne du département.</p>
<p>Après avoir ouvert votre session Windows, modifiez la connexion réseau physique de votre poste de travail comme dans l’image qui suit:</p>
<p><img src="../Images/conn-eth.jpg" alt="conn-eth"></p>
<p>Dans ce réseau, vous avez accès à internet, mais les ressources du Collège sont limitées.</p>





<blockquote class="gdoc-hint note">
  <div class="gdoc-hint__title flex align-center"><i class="fa note" title="Attention"></i></div>
  <div class="gdoc-hint__text">A la fin du cours, n’oubliez pas de rebrancher le câble sur le réseau du Collège!</div>
</blockquote>

<div class="gdoc-page__anchorwrap">
    <h2 id="connexion-de-vscode">
        Connexion de VSCode
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/installation/EnvDistant/#connexion-de-vscode" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Connexion de VSCode" aria-label="Anchor to: Connexion de VSCode" href="#connexion-de-vscode">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Votre serveur est identifié par votre prénom suivi du domaine “.lan”, par exemple <em><strong>olivier.lan</strong></em>. L’application <em>React</em> de base et la librairie <em>Bootstrap</em> y sont installées. Pour vous connecter au serveur à partir de <em>VSCode</em> pour la première fois, vous devez créer la connexion comme suit:</p>
<p><img src="../Images/newconnection.png" alt="newconnection"></p>
<p>Puis choisir <code>+ Add New SSH Host...</code> dans les options disponibles. Entrez ensuite la commande de connexion sur votre serveur. Par exemple pour le serveur <em>olivier.lan</em>, la commande est la suivante:</p>
<p><img src="../Images/commandeconnect.png" alt="commandeconnect"></p>
<p>Puis sélectionnez le fichier de votre choix pour sauvegarder les informations de connexion.</p>





<blockquote class="gdoc-hint note">
  <div class="gdoc-hint__title flex align-center"><i class="fa note" title="Note"></i></div>
  <div class="gdoc-hint__text">Le mot de passe initial est <code>abc-123</code>; il est fortement recommandé de le changer. Pour ce faire utilisez la commande <code>passwd</code> à partir du terminal.</div>
</blockquote>

<p>L’environnement de développement comprend une instalation de <em>NodeJS</em>, <em>Bootstrap</em> et l’application par défaut (“Hello World”) de <em>React</em>.</p>
<div class="gdoc-page__anchorwrap">
    <h2 id="démarrage-de-lapplication-react">
        Démarrage de l’application React
        <a data-clipboard-text="http://otardi.gitlab.io/420-211/installation/EnvDistant/#démarrage-de-lapplication-react" class="gdoc-page__anchor clip flex align-center" title="Anchor to: Démarrage de l’application React" aria-label="Anchor to: Démarrage de l’application React" href="#d%c3%a9marrage-de-lapplication-react">
            <svg class="gdoc-icon gdoc_link"><use xlink:href="#gdoc_link"></use></svg>
        </a>
    </h2>
</div>
<p>Pour démarrer l’application, faites les comandes suivantes:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="cd /var/www
npm start" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-bash" data-lang="bash"><span class="line"><span class="cl"><span class="nb">cd</span> /var/www
</span></span><span class="line"><span class="cl">npm start
</span></span></code></pre></div>




<blockquote class="gdoc-hint caution">
  <div class="gdoc-hint__title flex align-center"><i class="fa caution" title="Attention"></i></div>
  <div class="gdoc-hint__text"><p>L’erreur suivante peut survenir lorsque vous faites <code>npm start</code>:</p>
<blockquote>
<p>Error: ENOSPC: System limit for number of file watchers reached</p>
</blockquote>
<p>Si c’est le cas, lancez les commandes suivantes:</p>
<div class="highlight gdoc-post__codecontainer"><span class="flex align-center justify-center clip gdoc-post__codecopy" data-clipboard-text="echo 'fs.inotify.max_user_watches=524288' >> /etc/sysctl.conf
sysctl -p" data-copy-feedback="Copied!" role="button" aria-label="Copy"><svg class="gdoc-icon copy"><use xlink:href="#gdoc_copy"></use></svg><svg class="gdoc-icon check hidden"><use xlink:href="#gdoc_check"></use></svg></span><pre tabindex="0" class="chroma"><code class="language-bash" data-lang="bash"><span class="line"><span class="cl"><span class="nb">echo</span> <span class="s1">'fs.inotify.max_user_watches=524288'</span> &gt;&gt; /etc/sysctl.conf
</span></span><span class="line"><span class="cl">sysctl -p
</span></span></code></pre></div></div>
</blockquote>

<p>L’application sera visible au port 3000 du serveur; donc si votre serveur se nomme <em><strong>tom.lan</strong></em>, ouvrez une page à l’adresse <a class="gdoc-markdown__link" href="http://tom.lan:3000">http://tom.lan:3000</a>:</p>
<p><img src="../Images/hellotom.png" alt="hello"></p>

  </article>
