Demande d'un certificat personnel IGTF
======================================

Introduction
------------

Cette documentation décrit la procédure d'obtention d'un certificat
personnel IGTF (TCS) [1]_ nécessaire pour utiliser l'infrastructure de
grille de calcul de France Grilles.

Ce certificat permet d'accéder :

* aux ressources de calcul HTC

* aux espaces de stockage

* aux sites web sécurisés.

Pour plus d'informations générales sur les certificats TCS, RENATER
maintient une documentation officielle [2]_.

**Important :** L'utilisateur est responsable du stockage sécurisé
et de la sauvegarde de sa clé privée. Toute perte ou compromission
nécessite la révocation du certificat.

Condition d'éligibilité
-----------------------

La délivrance d'un certificat personnel IGTF est réservée aux agents
disposant d'un identifiant valide d'un établissement public de
l'Enseignement Supérieur et de la Recherche.

Procédure d'obtention du certificat
-----------------------------------

Pour obtenir un certificat, il faut suivre les étapes suivantes :

1. Se rendre sur le portail HARICA : https://cm.harica.gr/

2. Se connecter en utilisant le bouton "Academic Login".

3. S'authentifier avec vos identifiants d'établissement (CNRS, CEA,
   INRAE, Université, ...).

4. Dans le menu de gauche, sélectionner "IGTF Client Auth" .
   Trois types de certificats vous sont proposés. Choisir :
    "GÉANT Personal Authentication", puis cliquer sur "Next".

5. Lire et accepter les conditions d'utilisation, puis cliquer sur
   "Submit Request".

6. Sur l'écran suivant, cliquer sur "Enroll your Certificate".

7. Conserver les valeurs par défaut, puis :

   * Définir un mot de passe robuste [3]_
   * Confirmer que vous êtes le seul détenteur de ce mot de passe
   * Cliquer sur "Enroll Certificate".

8. Cliquer sur "Download" pour télécharger votre certificat.

**Important** : le certificat ne peut être téléchargé qu'une seule
fois. Le fichier est fourni au fomrat PKCS#12 sous le nom :
``Certificate.p12``.


Durée de validité et renouvellement
-----------------------------------

Le certificat personnel IGTF délivré via le portail HARICA a une durée
de validité limitée (**1 an** à compter de sa date d'émission).

Il est de la responsabilité du titulaire :

* de vérifier la date d'expiration de son certificat ;
* d'anticiper son renouvellement avant son échéance ;
* de ne pas utiliser un certificat expiré pour accéder aux
  infrastructures de calcul ou de stockage.

Le renouvellement s'effectue en suivant la même procédure que pour une
première demande. Il est recommandé d'engager la démarche plusieurs
jours avant la date d'expiration afin d'éviter toute interruption de
service.


Révocation du certificat
------------------------

La révocation d'un certificat est obligatoire dans les cas suivants :

* perte du fichier ``Certificate.p12`` ;
* oubli ou compromission du mot de passe protégeant la clé privée ;
* suspicion d'accès non autorisé à la clé privée ;
* départ de l'établissement ou changement d'affiliation.

En cas de compromission ou de doute sur la confidentialité de la clé
privée, le certificat doit être révoqué **sans délai**.

La demande de révocation doit être effectuée à travers l'interface
HARICA. Depuis le tableau de bord, cliquer sur les trois points
verticaux à droite du certificat concerné, puis sélectionner "Revoke".

Après révocation, un nouveau certificat devra être généré en suivant
la procédure décrite ci-dessus.


En cas de problème
------------------

En cas de difficultés lors de la génération du certificat, vous pouvez
contacter votre point de contact pour la délivrance des certificats. Si
vous ne le connaissez pas, contacter directement le support RENATER [3]_.

Conversion et import
--------------------

Le certificat téléchargé est au format PKCS12. Il peut :

* être importé directement dans un navigateur [5]_ ;

* transformé au format X.509 pour utilisation avec les outils de
  grille [6]_.


.. [1] Certificat TCS : https://wiki.geant.org/display/TCSNT/TCS+wiki+%282020%29+Sectigo

.. [2] Documentation RENATER sur les certificats : https://services.renater.fr/tcs/index

.. [3] Recommandation de l'ANSSI concernant les mots de passe : https://cyber.gouv.fr/cybermois-2021-les-mots-de-passe

.. [4] Support RENATER : https://services.renater.fr/tcs/contact-support

.. [4] Chargement d'un certificat dans le navigateur : https://services.renater.fr/tcs/faq/tcs_personnes/export_import#importer_une_sauvegarde_de_certificat_dans_mon_navigateur

.. [5] Conversion d'un certificat : https://doc.cc.in2p3.fr/fr/Daily-usage/certificate.html#certificate
