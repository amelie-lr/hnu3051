---
title: "Développer une écriture consciente avec le Markdown"
date: 2023-04-25
revision: 
toc: true
categories: ["Travail étudiant"]
tags: ["markdown", "infographie", "archivistique", "écriture"]
cours: "HNU3000 - Humanités numériques : Laboratoire"
prof: "Michael E. Sinatra"
session: "hiver 2023"
bibfile: content/posts/2023-hnu3000-markdown.json
---


*Ce texte a été rédigé en Markdown avec le logiciel MacDown.*

L'arrivée relativement récente du numérique dans nos vies en bouleverse certaines habitudes. L'ordinateur, pourtant machine à calculer à l'origine, s'est depuis transformé en machine à écrire. Mais l'écriture numérique n'est pas la même que l'écriture sur papier. En appuyant sur les touches, nous ne faisons que guider la machine afin qu'elle se charge d'écrire en code binaire sur le disque.

Les interfaces graphiques des traitements de texte forment un écran entre nous et l'écriture qui se passe derrière, une couche supplémentaire là pour nous simplifier la tâche grâce au WYSIWYG (*What you see is what you get*), mais qui fait en sorte que nous sommes moins conscients de ce que la machine écrit réellement, soit du «code» souvent complexe.

Une alternative aux interfaces graphiques est le Markdown, plutôt basé sur le WYSIWYM (*What you see is what you mean*) et qui privilégie une sémantique sans ambiguïtés au lieu du style.




## Qu'est-ce que le Markdown?

Le Markdown est un langage de balisage léger créé par John Gruber et Aaron Swartz en 2004. Par l'ajout d'une syntaxe simple à du texte non formaté (texte brut), il permet de simplifier l'écriture numérique tout en y intégrant une sémantique. Les fichiers `.md` sont compatibles avec tout logiciel capable de lire le format texte (`.txt`), que ce soient des éditeurs de texte qui ne peuvent gérer que du texte, par exemple TextEdit et Bloc-Notes (Notepad), ou des traitements de texte plus axés sur la bureautique[^perret]{{< cite "perretFormatTexte2023" >}}, comme Word. Cet avantage fait en sorte qu'un texte structuré en Markdown est supporté par de nombreux outils. Il n'a d'ailleurs pas besoin d'être interprété par un logiciel pour être lisible (par l'humain), même si sa syntaxe est apparente, ce qui en fait un format d'écriture plus pérenne. Plusieurs outils ont tout de même été développés à partir du Markdown, dans le but d'offrir une interface de prévisualisation par exemple.

[^perret]: Perret, A. (2023). *Format texte*. Consulté le 20 avril 2023. [https://www.arthurperret.fr/cours/format-texte.html](https://www.arthurperret.fr/cours/format-texte.html)



### À qui s'adresse-t-il?

Le Markdown a été originalement conçu pour le web, plus particulièrement afin de faciliter le processus d'écriture dans les blogues, forums de discussion ou encore pour la rédaction de documentation. Il offre une conversion vers le HTML, dont le balisage est beaucoup plus verbeux.

![Comparaison HTML / Markdown / Web](https://images.ctfassets.net/2kgt0da0ld2o/2h5h8TtAQWWn8UZMBQsdZO/9df74e48e9125bfa1e3856f4e8f4ef3b/HTML-Markdown-TheBrain_comparison.png)
*Source : [The Brain](https://www.thebrain.com/blog/markdown-vs-html)*

Maintenant, ce sont auteurs, blogueurs et étudiants qui l'utilisent autant pour la rédaction d'articles ou de travaux de recherche que pour la prise de notes.


## En pratique

### Comparaison avec Word

Afin de mieux comprendre les avantages du Markdown, voyons d'abord ce qui se cache derrière une écriture faite dans Word et sauvegardée au format `.docx`. En remplaçant l'extension de fichier d'un document Word par `.zip` puis en le décompressant, cela nous permet de découvrir de quoi ce fichier est réellement constitué[^word]. Voici donc un exemple de code généré pour un article simple[^note].

[^word]: Voici [comment s'y prendre](https://superuser.com/questions/539919/view-source-equivalent-for-word-documents), un truc que j'avais appris alors qu'un client s'entêtait à nous fournir ses images dans un fichier Word.

[^note]: L'article a été pris sur le web dans le cadre d'un exercice. Il a d'abord été formaté en Markdown en ajoutant un peu de formatage qui n'était pas présent dans l'original (par exemple l'ajout d'une image et la conversion d'un paragraphe en liste), puis reformaté dans Word en utilisant les feuilles de styles par défaut afin de recréer exactement la même structure de texte le plus simplement possible.

![test Markdown](https://github.com/amelie-lr/hnu3000_projet/blob/main/images/test_word.png?raw=true)
*Code source du fichier Word (`document.xml` -- 25 Ko)*

Pour exactement le même texte avec la même structure, voici maintenant le code en Markdown.

![test Word](https://github.com/amelie-lr/hnu3000_projet/blob/main/images/test_markdown.png?raw=true)
*Code source du fichier Markdown (`document.md` -- 8 Ko)*

Pour la majorité des gens qui utilisent Word, il peut y avoir confusion entre le fond (la structure du texte) et la forme (son rendu graphique)[^fauchie]{{< cite "fauchieHNU2000HumanitesNumeriques2022" >}}. Car ce que l'on voit dans le logiciel n'est que l'interprétation faite du code écrit par la machine. À l'ère du numérique, on nous habitue aux interfaces graphiques par souci de nous rendre la tâche plus simple. Mais est-ce vraiment le cas? De nos jours, il est fort à parier que Word est le traitement de texte le plus répandu. Or, apprendre à écrire avec Word ne sert qu'à écrire avec Word malheureusement. 

[^fauchie]: Fauchié, A. (2022). *HNU2000 Humanités numériques : technologies -- Séance 5 -- Écrire*. [https://hnu2000.quaternum.net/seance-05-ecrire/](https://hnu2000.quaternum.net/seance-05-ecrire/)

L'apprentissage du Markdown, quant à lui, peut servir dans de multiples applications. D'autant plus que son balisage simple permet de le maitriser très rapidement. Au lieu d'apprendre comment écrire avec différents outils, le langage utilisé reste le même et c'est plutôt l'outil qui génère la sortie qui change. Ceci nous permet alors de n'avoir qu'une seule source pour plusieurs sorties (PDF, site web, imprimé). 

L'écosystème qui gravite autour, plutôt axé vers le `code` d'une vue extérieure, pourrait toutefois rebuter certaines personnes moins à l'aise avec cette perspective. Il demeure cependant un point de départ accessible vers une meilleure littératie numérique. Les interfaces graphiques, bien que pratiques, ne permettent malheureusement pas de bien saisir (et donc de maitriser) ce qui se passe dans notre acte d'écriture à l'ère numérique.



### Mon expérience avec le Markdown

Il y a neuf mois, je n'avais jamais entendu parler du Markdown et pourtant maintenant je considère bien le maitriser. J'ai pu l'expérimenter avec plusieurs outils tels que :

- Stylo, une plateforme d'écriture en ligne;
- Hedgedoc, une autre plateforme axée sur les notes collaboratives;
- R Studio, VSCodium et Jupyter Notebooks pour de la programmation et qui supportent plusieurs autres systèmes de balisage comme le HTML, Javascript, CSS, YAML, JSON et j'en passe;
- Pandoc pour la conversion Markdown vers PDF entre autres;
- Hugo, un générateur de site statique permettant de convertir le Markdown en code HTML; et
- MacDown, un éditeur de texte pour MacOS.


### Difficultés rencontrées

Bien sûr, le Markdown a ses limites. Certaines balises pourraient être ajoutées, par exemple pour l'affichage d'une légende sous les images[^legende], définir une introduction ou encore pour intégrer quelques métadonnées que l'on voudrait afficher comme le nom de l'auteur et la date. Il est important de savoir que l'interprétation des balises peut aussi différer selon l'outil utilisé. Dans le cas des liens internes, soit vers une autre partie du texte dans lequel on se trouve, la syntaxe `[En pratique](#En-pratique)` fonctionne sur HedgeDoc, mais pas dans MacDown ni Stylo.

> [Cliquez ici pour **peut-être** être redirigé vers la section «En pratique»](#En-pratique)

[^legende]: À noter que Stylo affiche déjà le texte alternatif à titre de légende.

C'est le cas aussi pour les notes de bas de page. La syntaxe de base suivante semble fonctionner partout :

```
Voici du texte avec une note de bas de page[^nom]

[^nom]: Ceci est une note de bas de page
```

> Voici du texte avec une note de bas de page[^nom]

[^nom]: Ceci est une note de bas de page

Mais la méthode *inline*, que je trouve personnellement plus simple, fonctionne dans Stylo et HedgeDoc, mais pas dans Hugo ni MacDown.

```
Voici du texte avec une note de bas de page^[Note de bas de page inline]
```

> Voici du texte avec une note de bas de page inline^[Note de bas de page inline]

Considérant que le Markdown est tout de même assez récent et encore en développement, il est donc normal que l'implémentation dans les outils ne soit pas uniforme. Il existe d'ailleurs différentes variantes (*flavors*) du langage. Un effort de standardisation a heureusement été lancé en 2012, puis c'est en 2014 qu'est né *CommonMark*[^commonmark]{{< cite "CommonMark" >}}, une initiative indépendante rassemblant des fans/utilisateurs intensifs œuvrant dans des entreprises d'outils numériques où le Markdown est bien implémenté, qui ont élaboré un recueil de spécifications afin d'éliminer les ambiguïtés. On n'y traite pas de la syntaxe en tant que telle, mais plutôt de sa conversion vers le HTML.

[^commonmark]: CommonMark. (s. d.). Consulté le 16 avril 2023. [https://commonmark.org/](https://commonmark.org/)




## Les possibilités

Malgré ces petits défauts, je compte tout de même continuer à utiliser le Markdown et revoir mon processus d'écriture en remplaçant certains outils propriétaires et fermés par des alternatives libres et ouvertes (et avouons-le, gratuites). Au fil de mes expériences avec ce langage, je me suis constamment posé la question s'il pouvait être possible d'un jour convertir l'ensemble de la population à cette forme d'écriture que je considère plus consciente et favorisant la littératie numérique. Je rêve en quelque sorte à le propager aux organismes publics et aux entreprises. Mon cheminement de carrière m'a mené à côtoyer deux domaines et je vois dans les deux les avantages qu'apporterait l'intégration du Markdown dans les pratiques. Je vous présente donc ma vision sous deux points de vue.


### Point de vue de l'infographiste

Après 20 ans en communications graphiques, me voilà tranquillement à me détacher de cette structure graphique à la sémantique souvent purement visuelle. Je me considère définitivement comme une personne visuelle, mais ce côté créatif ne m'empêche pas d'être très structurée. L'expression «Pourquoi faire ça simple quand on peut faire ça compliqué?» ne s'applique d'ailleurs pas du tout à moi. Ce qui explique probablement mon intérêt improbable envers le Markdown.

Disons-le tout de suite, je n'ai jamais été fan de Word, principalement parce que je connais InDesign, un **vrai** logiciel de mise en page. En tant qu'infographiste pour des boites de design corporatif, trop de fois je me suis fait demander de préparer des gabarits Word avec une belle mise en page en colonnes, par exemple. Avec le temps, j'ai appris à connaître les limites et caprices de Word. Or, les personnes qui utilisent ces gabarits par la suite maitrisent rarement bien l'outil. Et contrairement à ce que plusieurs semblent penser, Word n'est pas un logiciel de mise en page! Pourtant on s'efforce de rendre ces documents jolis, avec une belle typographie et quelques niveaux de titres, en oubliant malheureusement que le rendu visuel est souvent vide de sémantique derrière. Comme on nous apprend à voir au-delà de l'apparence d'une personne, j'ai appris à voir les dessous d'un document. 

Apprendre le Markdown aux clients pourrait simplifier grandement la chaine éditoriale. Le processus actuel ressemble à celui-ci :

1. Le client fournit un ou des documents Word où les feuilles de styles sont rarement bien utilisées pour structurer le texte.
2. Le designer importe les contenus en texte brut en ne conservant pas le formatage ni le lien avec la source.
3. Il applique ses nouvelles feuilles de style et reformate tous les gras, italiques.
4. La mise en page est relue à l'interne pour s'assurer que tout est conforme à l'original reçu.
5. Le client attend de recevoir une première épreuve sur laquelle il inscrit ensuite ses corrections au texte, car les textes sont rarement vraiment finaux quand on les reçoit.
6. S'en suit un va-et-vient de corrections jusqu'à l'approbation du texte et de la mise en page finaux.

Des fonctions d'InDesign permettent de garder le lien avec le texte original et faire concorder les styles du fichier Word avec ceux du document InDesign, mais comme mentionné à la première étape, les documents reçus sont souvent tellement mal structurés qu'il est beaucoup plus simple de recommencer à zéro.

> InDesign’s linked file placement workflow assumes that the original document has been correctly formatted to start with. Indeed, few Word users know of its styles (header, subheading, emphasis, etc.) — let alone they apply them consistently. Instead, people are doing all sorts of weird stuff while playing around with Word’s wysiwyg click-a-button tricks.
> 
> *Dr Wouter Soudan*[^indd]{{< cite "soudanWordMarkdownInDesign" >}}

Mais si le client rédigeait son texte en Markdown déjà sémantisé, le designer pourrait alors se concentrer sur la préparation du modèle qui recevra le texte et ce dernier n'aurait ensuite qu'à y importer le texte, en conservant le lien vers le fichier placé idéalement dans un environnement partagé entre client et designer, et le logiciel se chargerait automatiquement (ou à l'aide de scripts) de convertir la sémantique en appliquant les styles correspondants. Une recherche rapide à savoir s'il existait déjà une intégration Markdown/InDesign m'a mené à [cet article du Dr Wouter Soudan](http://rhythmus.be/md2indd/), un typographe belge qui explique exactement ce que j'avais en tête. Les avantages de cette façon de faire seraient le travail en parallèle, donc l'économie de temps, la simplification du flux de travail ainsi que la possibilité d'utiliser un seul et même contenu original (entrée) pour générer plusieurs sorties, par exemple un rapport d'activités en PDF, imprimé et présenté dans un site web. On parle ici de *single source publishing*, un modèle plus efficace.

[^indd]: Soudan, W. (s. d.). *From Word to Markdown to InDesign*. Consulté le 20 avril 2023. [http://rhythmus.be/md2indd](http://rhythmus.be/md2indd)


### Point de vue de l'archiviste

Nouvelle venue dans le domaine de l'archivistique, mes études en humanités numériques m'ont permis de constater à quel point les avancées numériques sont importantes à prendre en compte, et ce autant pour les archives anciennes, que l'on numérise afin d'en faciliter l'accès, que pour les récentes et futures archives nées numériques qu'il faudra savoir gérer à long terme. Le développement des technologies est de plus en plus rapide, de nouveaux formats et standards apparaissent puis disparaissent aussi vite. Dans cette optique, quelle place peut prendre le balisage Markdown?

Le format `.docx` de Word, pourtant très répandu, demeure un format propriétaire, axé sur des intérêts commerciaux, ce qui laisse flotter certaines préoccupations quant à sa pérennité, car Microsoft peut en faire ce qu'elle en veut. C'est pourquoi Bibliothèque et Archives nationales du Québec le considère comme un format acceptable (et non favorisé) pour les documents textuels dans son *Guide concernant les formats recommandés par BAnQ*.

> BAnQ se base sur les critères suivants afin de déterminer la viabilité à long terme des formats :    
> 
> - l'accessibilité et l'exhaustivité de la documentation : un format doit être doté d’une documentation complète et accessible;
> - la fréquence d'utilisation : un format très utilisé et populaire a plus de chances d'être utilisé longtemps;
> - le  degré d'ouverture : un format ouvert est lisible par plusieurs logiciels; un format propriétaire est souvent lié à un seul logiciel;
> - la reconnaissance du format : lorsqu’un format est reconnu par une norme, il est adopté plus largement et sa documentation est plus accessible.
>
> *Source : Bibliothèque et Archives nationales du Québec (2020)*[^banq]{{< cite "bibliothequeetarchivesnationalesduquebecGuideConcernantFormats2020" >}}

[^banq]: Bibliothèque et Archives nationales du Québec. (2020, mars). *Guide concernant les formats recommandés par BAnQ*. Consulté le 22 avril 2023. [https://numerique.banq.qc.ca/patrimoine/details/52327/4076856](https://numerique.banq.qc.ca/patrimoine/details/52327/4076856)

Le format texte, quant à lui, vient en tête de liste, entre autres parce qu'il ne dépend pas d'une technologie en particulier pour être lu. Le Markdown s'y apparentant, tel que mentionné précédemment, il n'y a donc pas lieu de s'inquiéter pour sa pérennité. Et même s'il advenait que ce langage soit mis de côté pour une alternative jugée meilleure, il restera lisible autant par la machine que par l'humain grâce à son balisage léger. L'aspect de la légèreté ne s'arrête pas là puisqu'il est aussi plus léger en termes de stockage comparativement à son équivalent `.docx` tel que vu plus haut (voir *[Comparaison avec Word](#Comparaison-avec-Word)*). Même si l'espace disque nous semble infini de nos jours, cette idée nous amène justement à produire encore plus de documents et cette croissance exponentielle n'est pas sans impact, en termes de consommation d'énergie et sur l'environnement entre autres. 

Tel que démontré, le Markdown pourrait être une solution à mettre en place en vue de favoriser la conservation et l'accessibilité à très long terme de nos futures archives historiques nées numériques. Par son format libre et ouvert, son interopérabilité et sa simplicité d'apprentissage, nul doute qu'il trouverait sa place dans ce nouveau monde technologique où formats de fichiers et supports deviennent trop rapidement obsolètes. Les futurs archivistes nous en remercieront.



## Conclusion

Même si le Markdown fût développé principalement pour l'écriture sur le web en alternative aux interfaces WYSIWYG (*What you see is what you get*), je crois de plus en plus qu'il pourrait s'adapter bien au-delà. L'écriture numérique n'est pas seulement en ligne après tout. Par exemple, déjà les universitaires s'approprient le langage parce qu'il facilite la rédaction de leurs travaux et de leurs notes[^scholars]{{< cite "shieberSwitchingMarkdownScholarly2014" >}}. Le Markdown ne répond probablement pas à tous les besoins particuliers pour le moment, comparativement aux traitements de texte nous offrant multiples fonctions tout-en-un, mais rien n'empêche de développer des outils autour pour y répondre. C'est le cas pour la production de présentations pour lesquelles bon nombre d'outils existent déjà[^pres]{{< cite "siddiquiUltimateListMarkdown2021" >}}. Ce modèle modulaire offre beaucoup plus de flexibilité quand on y pense.

[^scholars]: Shieber, S. (2014, 29 août). Switching to Markdown for scholarly article production. *The Occasional Pamphlet*. Consulté le 23 avril 2023. [https://blogs.harvard.edu/pamphlet/2014/08/29/switching-to-markdown-for-scholarly-article-production/](https://blogs.harvard.edu/pamphlet/2014/08/29/switching-to-markdown-for-scholarly-article-production/)

[^pres]: Siddiqui, L. (2021, 24 octobre). The Ultimate List of Markdown Presentation Tools. *Tiiny Host Blog*. Consulté le 23 avril 2023. [https://tiiny.host/blog/the-ultimate-list-of-markdown-presentation-tools/](https://tiiny.host/blog/the-ultimate-list-of-markdown-presentation-tools/)


Dans le cours FRA3825 -- Pratiques de l'édition numérique, à la séance où Margot Mellet nous présentait le Markdown, j'ai noté ceci : «responsabilisation de l'humain dans l'écriture». Les interfaces graphiques ont peut-être favorisé la démocratisation de l'écriture numérique, mais le Markdown pourrait nous aider à comprendre ce que nous écrivons.




## Bibliographie

{{< bibliography >}}

Getting Started. (s. d.). *Markdown Guide*. Consulté le 15 avril 2023. [https://www.markdownguide.org/getting-started/](https://www.markdownguide.org/getting-started/)

Gruber, J. (s. d.). *Markdown*. Daring Fireball. Consulté le 16 avril 2023. [https://daringfireball.net/projects/markdown/](https://daringfireball.net/projects/markdown/)

*Markdown*. (2023, 7 mars). Dans *Wikipedia*. Consulté le 15 avril 2023. [https://en.wikipedia.org/wiki/Markdown](https://en.wikipedia.org/w/index.php?title=Markdown&oldid=1143363892)


