---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Foire aux questions : serveurs (informations générales)
{: #faqs-servers-general-}

## Quelle est la différence entre les fonctions "Initialiser à partir d'une image" et "Charger à partir d'une image" ?
{:faq}

Les fonctions Initialiser à partir d'une image et Charger à partir d'une image utilisent des modèles d'image qui sont appliqués à un terminal pour remplacer le système d'exploitation existant ou pour aider ce dernier lorsqu'il tente de résoudre un problème existant. Seul, le type d'image utilisé est différent pour ces deux processus. Lorsque vous exécutez un de ces processus, vérifiez que vous avez sauvegardé toutes les données que vous souhaitez restaurer.

   * La fonction Initialiser à partir d'une image permet d'initialiser un terminal en utilisant une image ISO fournie par {{site.data.keyword.BluSoftlayer_full}} pour la reprise du système ou une image ISO téléchargée via la fonction *Importer image* dans la console {{site.data.keyword.cloud_notm}}. L'image ISO peut être une version propre du système d'exploitation du terminal ou un disque de reprise pouvant être utilisé lors d'une tentative de résolution d'un problème lié au terminal.
   * La fonction Charger à partir d'une image est une méthode de rechargement du système d'exploitation qui utilise un modèle d'image ayant été capturé sur une unité ou téléchargé via la fonction *Importation d'image* de la console {{site.data.keyword.cloud_notm}}. L'option *Charger à partir d'une image* effectue le rechargement en utilisant un VHD, qui retire du terminal toutes les données et remplace les fichiers et le système d'exploitation existants par une version de l'image sélectionnée semblable à celle d'origine.

## Pourquoi ne puis-je pas me connecter à la console KVM ?
{:faq}

Si vous ne pouvez pas vous connecter à la console KVM, consultez les conseils d'identification et de résolution des problèmes ci-dessous pour résoudre plus facilement le problème. Si des problèmes supplémentaires surviennent, contactez le support technique. Pour savoir comment procéder, voir [Aide et support](/docs/vsi?topic=virtual-servers-gettinghelp#gettinghelp).

   * La console KVM est une applet Java. Pour pouvoir accéder à la console, Java doit être installé. Pour plus d'informations sur l'installation de Java, voir [Free Java Download ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.java.com/en/download/){: new_window}.  
   * Si Java est installé, vérifiez qu'une connexion a été établie via VPN. Si aucune connexion n'est établie, un avertissement s'affiche lors de la tentative de connexion à la console KVM indiquant qu'une connexion VPN est requise.
   * La console KVM peut afficher une ou plusieurs fenêtres contextuelles lors du processus de connexion. Activez les fenêtres en incrustation à partir de la console {{site.data.keyword.cloud_notm}} pour vous assurer qu'il est possible d'établir une connexion.
   * Une erreur "Java applications are blocked by your security settings" peut s'afficher. Pour les terminaux iKVM Bare Metal, vous devez ajouter une exception pour l'adresse IP du terminal IPMI. Pour les terminaux VSI, vous devez autoriser "https://control.softlayer.com" et l'adresse IP de la machine KVM. Pour plus d'informations, voir [Why are Java applications blocked by your security settings with the latest Java? ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.java.com/en/download/help/java_blocked.xml){: new_window}.
   * Si les conditions ci-dessus sont respectées et que le message d'erreur "Missing required Permissions manifest in main.jar" s'affiche, les applets Java n'ont pas été activées dans le panneau de configuration Java. Ce paramètre constitue une précaution de sécurité et a été introduit par Oracle dans Java SE v7. Activez les applets dans le panneau de configuration pour résoudre ce problème.

     Si vous utilisez Mac OSX avec Google Chrome, voir Information and System Requirements for Installing and Using Mac Java 7 sur le site Web Java.
{:note}

   * Si vous tentez de vous connecter à une instance VSI via le programme Java standard et que seuls des messages d'erreur sont générés, vous pouvez également essayer d'utiliser VNC.

Si vous avez effectué toutes les vérifications ci-dessus et que vous ne pouvez toujours pas vous connecter à la console KVM, contactez le support afin de résoudre ce problème. Si une connexion à la console a été établie mais que des problèmes surviennent lors de la connexion au terminal, vérifiez que les données d'identification utilisées lors de l'accès au terminal sont valides. Si nécessaire, contactez l'administrateur de compte pour vérifier ces données.

## J'ai perdu le mot de passe d'accès au serveur. Comment puis-je le récupérer ?
{:faq}

Si le mot de passe d'administrateur ou de superutilisateur permettant d'accéder à votre serveur ne fonctionne plus, vérifiez les éléments suivants. Si nécessaire, consultez les instructions pour lancer une instance Rescue Kernel et réinitialisez votre mot de passe.

   * Avez-vous copié et collé le mot de passe ? Si la réponse est négative, effectuez cette action. Collez également le mot de passe dans un bloc-notes afin de vous assurer qu'aucun espace n'a été accidentellement copié avec le mot de passe.
   * Si le serveur inclut cPanel, est-il possible que cPHulk ait bloqué votre adresse IP en raison d'échecs de connexion ? Le cas échéant, vous pouvez accéder au serveur en utilisant la machine KVM ou IPMI et placer votre adresse IP sur liste blanche dans cPHulk en indiquant "/scripts/cphulkdwhitelist" suivi de votre adresse IP.
   * Quelqu'un a-t-il récemment tenté de changer le mot de passe du serveur en modifiant le mot de passe dans la console {{site.data.keyword.cloud_notm}} ? La modification du mot de passe dans la console {{site.data.keyword.cloud_notm}} modifie uniquement son affichage. Cela n'a aucune incidence sur le mot de passe utilisé par le serveur. En cas de problème, vous pouvez contacter l'équipe de support qui peut avoir accès au mot de passe d'origine.
   * Vous devez peut-être redémarrer dans le mode récupération de votre système d'exploitation pour être en mesure de réinitialiser votre mot de passe. Pour plus d'informations, voir [Lancement de Rescue Kernel](/docs/vsi?topic=virtual-servers-launching-rescue#launching-rescue).

Si toutes ces vérifications ont été effectuées et que vous ne pouvez toujours pas vous connecter au serveur en utilisant le mot de passe, contactez l'équipe de support en utilisant un ticket et demandez une réinitialisation du mot de passe. L'équipe de support devra redémarrer le serveur pour pouvoir réinitialiser le mot de passe. Soyez donc prêt à accepter ce redémarrage et/ou à indiquer une période de maintenance au cours de laquelle effectuer cette opération. La plupart des réinitialisations de mot de passe peuvent être effectuées en 15 minutes. Dans la console {{site.data.keyword.cloud_notm}}, vous pouvez créer un ticket en cliquant sur **Support > Créer un cas** et en sélectionnant le sujet *Comptes & accès*.

## Les partitions LVM sont-elles prises en charge en tant que système de fichiers valide ?
{:faq}

La gestion LVM permet la gestion logique des systèmes de fichiers dans Linux. Dans l'environnement {{site.data.keyword.BluSoftlayer}}, la gestion LVM n'est pas prise en charge en tant que schéma de partitionnement amorçable. Les instances de serveur virtuel ne peuvent pas être commandées avec LVM et la mise à disposition échoue pour l'importation d'images utilisant LVM en tant que partition d'amorçage. Si LVM est requis sur la partition d'amorçage, l'offre Bare Metal peut prendre en charge LVM lors de l'amorçage pour certains systèmes d'exploitation. Avec une configuration et un support de système d'exploitation appropriés, des disques VSI secondaires peuvent être utilisés pour les partitions LVM. Toutefois, il est important de noter que LVM n'est pas un système de fichiers pris en charge pour les modèles d'image ou l'image flexible. Si vous avez des questions supplémentaires, ouvrez un ticket auprès de l'équipe de support qui peut vous aider.

## Routes 161.26.0.0/16 préconfigurées sur les hôtes client
{:faq}

{{site.data.keyword.BluSoftlayer_notm}} active une nouvelle route sur tous les serveurs nouvellement mis à disposition pour la prise en charge de produits à venir.
   * La route désigne une adresse dans la plage 161.26.0.0/16 (161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255) sur le réseau privé dorsal.
   * Ce bloc IP est affecté à {{site.data.keyword.BluSoftlayer_notm}} par IANA et aucune promotion n'en sera faite sur le réseau Internet public.
   * Seuls les systèmes {{site.data.keyword.BluSoftlayer_notm}} seront traités hors de cet espace.
   * Les ACL sur les serveurs client, les serveurs virtuels et les passerelles Vyatta devront être mises à jour afin de permettre aux hôtes du client d'utiliser les services Infrastructure configurés avec des adresses IP se trouvant hors de cette plage.

## Ajout de nouveau routage pour différents systèmes d'exploitation
{:faq}

   <table>
   <CAPTION>Tableau 1. Ajout de routes par système d'exploitation</CAPTION>
   <THEAD>
   <TR>
   <th>Système d'exploitation</th>
   <th>Procédure</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Windows 2003 Standard et Entreprise</td>
   <td>
   Ajoutez la route persistante à partir de la ligne de commande en entrant :
   <blockquote>route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p</blockquote>
   <b>Remarque :</b> Remplacez 10.0.0.1 par l'adresse IP de votre passerelle privée.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Server Core
   </td>
   <td>
   Ajoutez la route persistante à partir de la ligne de commande en entrant :
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Remarque :</b> Remplacez 10.0.0.1 par l'adresse IP de votre passerelle privée.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Web, Standard, Entreprise et Datacenter</td>
   <td>
   Ajoutez la route persistante à partir de la ligne de commande en entrant :
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Remarque :</b> Remplacez 10.0.0.1 par l'adresse IP de votre passerelle privée.
   </td>
   </tr>
    <tr>
   <td>RedHat, Fedora et CentOS</td>
   <td>
   Créez une nouvelle route en éditant/créant le fichier suivant : <i>/etc/sysconfig/network-scripts/route-eth0</i>
   <p>Une fois ce fichier créé, vous devez y ajouter les informations suivantes : <i>161.26.0.0/16 via 10.0.0.1</i>
   </p>
   <b>Remarque :</b> Remplacez 10.0.0.1 par l'adresse IP de votre passerelle privée.
   </td>
   </tr>
   <tr>
   <td>Ubuntu et Debian</td>
   <td>
   A la fin de votre fichier <i>/etc/network/interfaces</i>, ajoutez la ligne suivante :
   <blockquote>
   up route add -net 161.26.0.0/16 gw 10.0.0.1
   </blockquote>
   <b>Remarque :</b> Remplacez 10.0.0.1 par l'adresse IP de votre passerelle privée.
   </td>
   </tr>
   <tr>
   <td>Vyatta</td>
   <td><i>set protocols static route 161.26.0.0/16 next-hop 172.16.0.26</i>
   <p>
   <b>Remarque :</b> Remplacez 172.16.0.26 par la passerelle du sous-réseau sur lequel se trouve la machine, qui doit être identique à la passerelle définie pour la route 10.0.0./8.</p>
   </td>
   </tr>
   <tr>
   <td>ESXi</td>
   <td>Utilisez la commande suivante pour ajouter la route à l'hôte ESXi :
   <blockquote>
   esxcfg-route -a 161.26.0.0/16 10.0.0.1
   </blockquote>
   <b>Remarque :</b> Remplacez 10.0.0.1 par l'adresse IP de votre passerelle privée.</td>
   </tr>
   <tr>
   <td>CoreOS</td>
   <td>Créez un fichier de route statique dans /etc/systemd/network nommé 10-static.network semblable à l'exemple suivant :
   <blockquote>
   [Route]
   Gateway=10.0.0.1
   Destination=161.26.0.0/16
   </blockquote>
   <b>Remarque :</b> Remplacez 10.0.0.1 par l'adresse IP de votre passerelle privée.</td>
   </tr>
   </TBODY>
   </table>

   <a name="top"></a>

## Est-il possible que le système de surveillance effectue une réinitialisation automatique et prévienne un technicien de support lorsque le serveur ne répond plus ?
{:faq}

Oui, sur l'ordre de notre service **Automated Reboot from Monitoring Failure**, vous pouvez configurer le système de surveillance afin qu'il réinitialise automatiquement le serveur et émette un ticket destiné à un technicien de support lorsqu'une alerte de surveillance est émise. **NOC Monitoring** est fourni en tant que service supplémentaire, dans lequel vous recevez une notification personnelle lorsqu'un problème de surveillance survient. Pour en savoir plus sur ces offres, voir [Server Monitoring ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/cloud/infrastructure/monitoring?cm_mc_uid=46846454197915580355142&cm_mc_sid_50200000=71138741559658182022){:new_window}.

## Qu'est-ce qu'un miroir cvsup ?
{:faq}

Vous pouvez effectuer une mise à jour à l'aide d'un miroir cvsup local exécuté pour vous. Assurez-vous que votre fichier .sup contient l'entrée suivante :

```
*default host=cvsup.service.softlayer.com
```
{:pre }

Les fichiers .dist sont également mis en miroir et disponibles sur freebsd.org. Vous pouvez ajouter la ligne suivante dans votre fichier */etc/make.conf* pour tenter en premier un téléchargement depuis le référentiel local :

```
MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"
```
{:screen }

Si le fichier ne se trouve pas à cet endroit, il suivra le fichier Makefile de port individuel et passera au miroir suivant.
