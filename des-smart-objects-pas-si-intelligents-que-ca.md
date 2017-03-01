---
  file: des-smart-objects-pas-si-intelligents-que-ca.md
  title: "Des « Smart objects » pas si intelligents que ça"
  author: Vincent JOBARD
  date: 2017-03-01
  category: IOT
  tags: iot,smart objects,objets connectés
--- 
<meta http-equiv='Content-Type' content='text/html; charset=utf-8' />

# Des « Smart Objects » pas si intelligents que ça

Le CES 2017 a eu lieu le mois dernier et ces jours-ci se déroule le Mobile World Congress à Barcelone. Force est de constater que l'Internet des Objets (_IdO_ en français, _IoT_ en anglais pour _Internet of Things_), est **LA** grande tendance du moment, les experts ne tarrissant pas d'éloges sur les prétendus services apportés par ces nouveaux objets augmentés, qu'ils n'hésitent pas à qualifier d' _« intelligents »_.

Ces nouveaux objets sont -ils si intelligents que cela ? Où sont-ils le symptôme inquiétant d'un pĥénomène marketing visant à confisquer peu à peu le droit de propriété remplacé par un usufruit payé au prix fort ?

## Les deux secteurs de l'IoT

Aujourd'hui il existe deux grands secteurs pour l'IOT :

- L'IoT industriel, appelé M2M (_Machine to Machine_). Dans ce secteur, un grand soin est apporté pour créer de l'intelligence locale pour l'entreprise. Les données recueuillies sont le plus souvent collectées en local et les objets **DOIVENT nécessairement communiquer entre eux** afin de crer l'intelligence nécessaire, entre autre, à la mainetenance prédictive et/ou préventive, permettre d'améliorer les performances industrielles, etc... De plus, les données recueillies étant sensibles, un effort est vraiment porté sur la sécurité, d'autant plus que souvent, une entreprise peut s'offrir les services de personnes gérant cette nouvelle infrastructure.

- L'IoT grand public (désigné le plus souvent comme _IoT_ tout court). Alors là on tombe dans le festival du gros n'importe quoi...

## Ce n'est pas l'aptitude à pouvoir communiquer qui fait l'intelligence

Si on écoute le discours de nombreux commentateurs, c'est cette nouvelle aptitude à pouvoir communiquer qui rendrait de facto les objets _« intelligents »_. Sauf que si l'aptitude à communiquer rendait intelligent, Twitter ne serait pas infectés de troll haineux. Pour générer de l'intelligence via la communication il est important que les individus (humains comme objets) tiennent à la fois compte du contexte dans lequel se déroule la communication mais aussi qu'ils soient en musure de communiquer entre eux.

Or pour le moment le modèle dominant est le suivant. Il faut à tout prix capter le consommateur dans un écosystème prétenduement complet, qui doit le plus possible couvrir l'intégralité de ses pré-supposés besoin. La bataille se fait donc à celui qui proposera le plus grand des écosystème, à base de partenariat entre le constructeur du bien, et des fournisseurs de services tiers. Ainsi on espère donc que cet écosystème forcera le consommateur à acheter toutes les gammes de la marque. Après tout, le modèle Apple semble lui avoir réussi, non ?

Le modèle Apple a pourtant ses limites, et ne s'addresse qu'à des fan boys inconditionnels. Or, en dehors des hipsters hypes, quel consommateur voudrait se retrouver prisonnier d'une marque afin d'apporter un semblant d'intelligence dans sa cuisine ? Devrait-je me limiter et n'acheter qu'ElectroLux, Whirlpool ou Miele pour que ma cuisine soit intelligente ?

Car bien évidement, si le constructeur de votre lave-vaisselle _MarqueA_, a signé des accord avec les fournisseurs _FA_, _FZ_, _FE_, _FR_, _FT_, _FY_ et que le constructeur de votre réfrigérateur _MarqueB_ a signé des accords avec les fournisseurs _FA_, _FB_, _FC_, _FD_, _FE_, _FF_, et _FG_, alors vous ne pourrez les connecter entre eux qu'aux travers des services fournis par _FA_ et _FE_. Pire encore, votre réfrigérateur enverra des données privée dans le cloud de _MarqueB_ en passant par votre boitier Internet (qui je le rappelle fait aussi office de routeur), les données seront envoyées sur le cloud de _FA_ et _FE_, puis transférées au cloud de _MarqueA_ pour finallement revenir vers votre lave-vaisselle en passant par votre boitier internet.

Je la refait pour nos amis Ops (NetOps, SysOps, DevOps) : Un serveur _B_ (celui du frigo) communique avec un serveur _A_ (celui du lave-vaisselle) **situé sur le même réseau local**, en envoyant sur un cloud public _MB_ des **données potentiellement sensibles**, qui transiteront ensuite vers au travers des cloud publics _FA_ et _FE_, puis _MA_ pour revenir sur le réseau local s'adresser au serveur _A_.

![](what1.gif)

Et bien évidément si l'un de ses prestataires ferme son service (ce qui n'arrive jamais, croix de bois croix de fer et vive AC/DC) c'est soit une partie de l'intelligence qui s'en va, soit votre appareil ne sait tout simplement plus communiquer (gné !), voire pire, votre appreil devient inutilisable lorsque toute la partie applicative est écrite côté cloud, un grand merci à AWS IoT ou Azure IoT pour cette apport à l'intelligence des objets.

![](facepalm.gif)

Autre problème de taille, si l'objet physique en tant que tel vous appartient bien, son système informatique, lui, est propriété du constructeur, et il ne vous sera pas permis de le modifier pour l'adapter à vos usages dans de nombreux cas. Relativement peu d'objets dit « intelligents » sont soit, au mieux, open-source/open-hardware, soit présentent une API ouverte et fort bien documentée, transformant de facto l'objet en plateforme de développement. Dans ce cas comment parler d' « intelligence », excepté sous un angle purement marketing ? et comment continuer à parler de propriété, puisque l'objet dans son ensemble, n'est plus vraiment vôtre. L'objet physique ne sert que de point d'accès à un service qui est la réelle valeur ajoutée. Subtilement nous sommes passé du droit de propriété au droit d'usage, et pourtant, le prix de l'objet en magasin a bien augmenté 

Il serait temps que l'IoT grand public murisse et se nourisse d'une partie du travail de réflexion du monde M2M. En effet, l'objet intelligent de demain devra forcément être un objet capable de s'adapter à l'usage, et pouvant s'intégrer sans effort dans l'écosystème du consommateur, il devra être une potentielle plateforme de développement, créant de nouveaux business model perturbateurs. C'est en apportant des applications sur l'objet téléphone que des Uber, AirBnB ou autres entreprises « disruptives » ont pu voir le jour. Il est aujourd'hui temps d'apporter des applications non pas sur le cloud en y connectant des objets, mais sur l'objet en lui-même pour que naissent d'autres révolutions. Ce n'est qu'à ce moment-là que nous pourront réellement parler d'objets intelligents et revenir au droit de propriété sur l'objet aujourd'hui spolié.

PS: Certains me feront remarquer que je n'ai pas abordé la partie sécurité de l'IoT grand public qui semble VRAIMENT poser problème. Effectivement, il y a beaucoup à dire et cette thématique sera abordée dans un prochain billet


