<h1>Sécurité Oauth2 OIDC et Keycloak 23</h1>
<p>
    <b><a href="https://www.keycloak.org/archive/downloads-23.0.7.html">1- Téléchargement de keycloack 23</a> </b> <br>
    <img src="assets/1.png" alt="">
</p>
<p>
    <b>2- Démarrage de keycloak</b> <br>
    Pour le faire il faut après avoir téléchargé keycloak, il faut crééer un répertoire tools sur le disque C où le déposer <br>
    <img src="assets/2.png" alt=""> <br>
    Il faut ensuite ouvrir ce répertoire à partir de l'invite de commande. Et saisir la commande suivante :
    <pre>kc.bat start-dev</pre><br> Cela aura pour effet de démarrage de keycloak. Une fois le démarrage terminé il faut l'ouvrir à partir du navigateur sur l'adresse suivante <pre>localhost:8080</pre> <br>
    <img src="assets/3.png" alt="">
</p>
<p>
    <b>3- Création d'un compte Admin</b> <br>
    Lors du lancement de la page, tu sera dirigé vers une page de création de compte admin. Tu créer le login et le mot de passe.
    <img src="assets/4.png" alt=""> <br>
    <img src="assets/5.png" alt="">
</p>
<p>
    <b>4. Créer un realm</b> <br>
    Pour creer un realm il faut se connecter à keycloak avec le compte admin qui vient d'être créer et cliquer sur la liste déroulante en haut à gauche. Une fois déroulé, il sera affiché le bouton créer un realm.
    <img src="assets/6.png" alt=""> <br>
    <img src="assets/7.png" alt="">
</p>
<p>
    <b>5. Créer un client à sécuriser</b> <br>
    Ici ont entend par client, l'application (web/mobile) qu'il faut sécuriser. <br>
    <img src="assets/8.png" alt="">
</p>
<p>
    <b>6. Créer un utilisateur</b> <br>
    <img src="assets/9.png" alt="">
</p>
<p>
    <b>7. Créer un role</b> <br>
    <img src="assets/10.png" alt="">
</p>
<p>
    <b>8. Affecter un role à un utilisateur</b> <br>
    Pour affecter un role à un utilisateur il faut que l'utilisateur ai déjà été créé puis le role également. <br>
    Il faut cliquer sur le menu utilisateur ensuite cliquer sur le nom de l'utilisateur à qui l'ont veut assigner un role. <br>
    <img src="assets/11.png" alt=""> <br>
    Une fois ces actions mené, tu clique sur l'onglet Role mapping dans l'interface qui est apparu. <br>
    <img src="assets/12.png" alt=""> <br>
</p>
<p>
    <b>9. Utilisation de postman</b> <br>
    Afin de pouvoir utiliser postman pour faire les tests il faut aller cliquer sur le menu Realm settings. Ensuite scroller jusqu'à atteindre le lien OpenID endpoint configuration.
    <img src="assets/13.png" alt=""> <br>
    Identifier sur la page qui va s'ouvrir le token_endpoint et le copier. <br>
    <img src="assets/14.png" alt=""> <br>
    <b>- Tester l'authentification avec le mot de passe</b> <br>
    <img src="assets/15.png" alt=""> <br>
    <img src="assets/16.png" alt=""> <br>
    <b>- Analyser les contenus des deux JWT Access Token et Refresh Token</b> <br>
    <img src="assets/17.png" alt=""> <br>
    <b>- Tester l'authentification avec le Refresh Token</b> <br>
    <img src="assets/15.png" alt=""> <br>
    <img src="assets/18.png" alt=""> <br>
    <b>- Tester l'authentification avec Client ID et Client Secret</b> <br>
    Pour ce faire, il faut au préalable aller sur client, cliquer sur le client souhaité, une fois cela effectuer il faut scroller jusqu'à atteindre la section Capability config et Client authentication qu'il faudra activer <br>
    <img src="assets/19.png" alt=""> <br>
    Ensuite retourner dans postman <br>
    <img src="assets/15.png" alt=""> <br>
    <img src="assets/20.png" alt=""> <br>
    
</p>