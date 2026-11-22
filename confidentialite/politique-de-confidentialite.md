# Politique de confidentialité de Central

_Version bêta 1.4 — dernière mise à jour : 22 novembre 2026_

Central est actuellement en **version bêta**. Cette politique décrit l'application telle qu'elle est distribuée aujourd'hui. Elle sera mise à jour à mesure que le service évolue, notamment à l'ouverture de nouvelles fonctions et lors de la création de la structure juridique qui exploitera Central.

Elle explique quelles données personnelles l'application Central (onglets Infos, Activités, Cosam, Coz et Profil) traite, pourquoi, avec qui elles sont partagées, combien de temps elles sont gardées et comment exercer vos droits.

## 1. Responsable du traitement

Le responsable du traitement est **Résiste Rayll MAKITA MPIKA**, porteur du projet Central. La structure juridique qui exploitera Central est en cours de création ; dès sa constitution, elle deviendra responsable du traitement et cette politique sera mise à jour en conséquence.

- Contact pour toute question sur vos données et pour exercer vos droits : **contact@centralworldapp.com**

## 2. Les données que nous traitons

Les accès sensibles du téléphone (contacts, position, micro, appareil photo, photos) ne sont demandés qu'au moment où vous utilisez la fonction concernée. Vous pouvez les refuser ou les retirer à tout moment dans les réglages du téléphone.

### 2.1 Compte et connexion
- Numéro de téléphone (votre identifiant) et pays du compte.
- Vérification du numéro : le code reçu par SMS est envoyé et vérifié par Firebase Authentication (Google). Pour se protéger des abus, Google peut afficher une vérification anti-robot (reCAPTCHA) sur une page Google. Central reçoit seulement la preuve que le numéro a été vérifié, jamais le code.
- Session : un jeton de session, conservé dans le coffre sécurisé du téléphone (Keychain iOS / Keystore Android). La liste de vos appareils connectés et leur date de connexion est visible dans Profil › Sécurité › Appareils et sessions, d'où vous pouvez les déconnecter.

### 2.2 Profil
- Nom, description et photo de profil, si vous les renseignez.
- Réglage « Visibilité du profil » (être suggéré et trouvable par votre nom).
- Indicateur de confiance calculé à partir des vérifications effectuées (numéro vérifié, identité vérifiée).

### 2.3 Infos (actualités)
- Vos centres d'intérêt et le réglage « Moins de contenus commerciaux ».
- Vos recherches d'actualités, traitées par nos serveurs dans le catalogue d'articles de Central.
- Les articles que vous aimez ou enregistrez, et votre progression dans « Apprendre aujourd'hui ».
- Des mesures de lecture liées à votre compte : articles affichés, ouverts ou cliqués, temps de lecture actif et profondeur de défilement. Elles servent à ordonner votre fil.
- Contenus de tiers : les images des articles sont chargées directement depuis les serveurs des éditeurs, et un article ouvert dans le lecteur intégré est chargé depuis le site de l'éditeur, qui peut déposer ses propres cookies et applique sa propre politique de confidentialité. Central ne contrôle pas ces traitements.

### 2.4 Activités
Si vous créez une activité (Bar, Commerce, Flotte, Hôtel, Immobilier) : son nom, son adresse et son logo si vous les renseignez, puis les informations que vous y gérez (membres, biens, réservations, locations, ventes). Vous êtes responsable des données de tiers que vous y enregistrez. Pour rejoindre une activité, vous pouvez scanner un code QR avec l'appareil photo.

Pour une activité Bar ou Commerce, le catalogue public et son code QR rendent visibles de toute personne qui les consulte, sans compte Central, le nom de l'activité et son catalogue (produits et prix).

### 2.5 Cosam : ouverture d'un compte de paiement
Ouvrir un compte en euros demande de vérifier votre identité. Les informations suivantes vous sont demandées, puis transmises à notre partenaire bancaire Swan, qui tient le compte :
- Identité : prénom(s), nom, date, pays, ville et code postal de naissance, nationalité.
- Coordonnées : adresse e-mail et adresse postale.
- Situation : situation professionnelle, tranche de revenu mensuel ; lorsque la réglementation l'exige, numéro d'identification fiscale, et indication du statut de « personne américaine » au sens fiscal (avec le numéro fiscal américain le cas échéant).
- Vérification d'identité : elle se fait sur une page sécurisée de Swan, qui recueille directement votre pièce d'identité et, le cas échéant, un selfie, et rend la décision. Central conserve le statut de cette vérification.
- Justificatifs : si Swan en réclame un, vous pouvez le photographier ou l'importer (JPG, PNG, HEIC, PDF) ; Central le transmet à Swan.
- Code de paiement : il protège vos opérations. Central n'en conserve qu'une empreinte cryptographique (HMAC-SHA256), jamais le code lui-même.

### 2.5 bis Cosam : utilisation du compte activé
Une fois votre compte activé, Central traite :
- votre solde et l'historique de vos opérations ;
- vos bénéficiaires (nom et IBAN pour un virement, numéro de téléphone pour un envoi Mobile Money) ;
- l'IBAN de votre compte, tenu par Swan ;
- vos transferts et paiements (montant, devise, bénéficiaire, motif, date, statut) et les reçus correspondants.

Recharges et envois :
- **Recharge par carte bancaire** : elle passe par Stripe. Votre numéro de carte est saisi dans le formulaire sécurisé de Stripe ; Central ne le reçoit ni ne le conserve. Central transmet à Stripe le montant de la recharge.
- **Recharge et envoi par Mobile Money** : ils passent par pawaPay. Central lui transmet le numéro de téléphone Mobile Money (le vôtre ou celui du bénéficiaire), le montant et la devise. pawaPay les transmet à l'opérateur Mobile Money du pays concerné (Bénin, Burkina Faso, Cameroun, Congo, Côte d'Ivoire, Gabon, Sénégal).

### 2.6 Contacts du téléphone (Coz)
Si vous l'autorisez, Coz lit les numéros de votre carnet d'adresses et les envoie à nos serveurs pour savoir lesquels correspondent à un compte Central. Le serveur ne renvoie que les numéros trouvés et ne conserve pas votre carnet. Les noms de vos contacts ne sont pas envoyés. Le bouton « Inviter » ouvre votre application SMS : rien ne passe par nos serveurs.

Pour déterminer qui peut voir vos statuts, Central conserve uniquement les correspondances entre comptes Central issues de la synchronisation de votre carnet : « vous avez ce compte Central dans vos contacts ». Nous ne conservons ni les numéros de votre carnet qui ne correspondent à aucun compte, ni les noms que vous donnez à vos contacts. Vos statuts sont visibles par les personnes avec qui vous êtes contacts mutuels (chacun a le numéro de l'autre dans son carnet) et par celles à qui vous avez déjà écrit en message privé ; une personne que vous avez bloquée ne les voit jamais. Ces correspondances sont mises à jour à chaque synchronisation (un contact retiré de votre carnet en disparaît), supprimées quand l'un des deux comptes change de numéro, et effacées dans les deux sens lors de la suppression de votre compte.

Dans Coz, votre numéro de téléphone est visible par les personnes à qui vous avez écrit en message privé. Il n'est jamais montré à quelqu'un qui vous a seulement ouvert une discussion, ni à une personne bloquée. Le nom de vos contacts tel qu'il figure dans le carnet de votre téléphone est lu sur l'appareil pour l'affichage et n'est jamais envoyé à Central.

### 2.7 Messagerie et appels (Coz)
- Vos messages, notes vocales, photos, vidéos, documents et statuts (visibles 24 heures), ainsi que les informations de vos groupes. **Les messages ne sont pas chiffrés de bout en bout** : ils sont chiffrés pendant le transport et stockés sur nos serveurs pour être remis à vos correspondants.
- Appels audio et vidéo : la communication passe directement entre les appareils quand le réseau le permet. Sinon — c'est fréquent sur les réseaux mobiles — elle passe par un serveur relais de Central, hébergé chez AWS à Paris. Le son et l’image restent chiffrés entre les deux appareils : le relais les transporte sans pouvoir les lire, et **aucun appel n'est enregistré.** Pour établir la connexion, votre appareil interroge un serveur de Central, qui voit votre adresse IP ; les identifiants qui ouvrent le relais sont créés pour chaque appel et expirent au bout de deux heures. Si ce serveur ne répond pas, l'application se rabat sur un serveur STUN de Google, qui voit alors votre adresse IP. Pour diagnostiquer la qualité des appels, nous enregistrons si un appel est passé en direct ou par le relais, sans adresse IP. L'historique de vos appels (date, correspondant, durée) est conservé pour l'onglet Appels.
- Position : seulement quand vous choisissez de la partager dans une discussion ; un point unique (latitude, longitude), sans suivi continu. Pour afficher l'aperçu de carte et l'adresse d'une position partagée, l'application transmet ce point au service de cartes du téléphone : **Apple** (Plans / MapKit) sur iPhone, **Google** (Google Maps) sur Android. Ce service ne reçoit ni votre nom ni le contenu de la discussion.
- Réglages : présence (« en ligne » et « vu à »), confidentialité avancée, personnes bloquées.
- Discussions verrouillées : la reconnaissance Face ID / empreinte a lieu sur votre appareil ; rien n'est transmis.

### 2.8 Notifications
Si vous les acceptez, un identifiant de notification de votre appareil est enregistré pour vous prévenir des nouveaux messages. Il est retiré à la déconnexion.

### 2.9 Données techniques
- Type d'appareil (mobile) et date de connexion de chaque session.
- Adresse IP : utilisée de façon transitoire pour limiter les abus (limitation du nombre de requêtes) et par nos journaux techniques de sécurité.

**Ce que Central ne fait pas :** aucun outil de mesure d'audience, de publicité ciblée ou de rapport de plantage tiers n'est intégré à l'application, et vos données ne sont pas vendues.

## 3. Finalités et bases légales

| Finalité | Données | Base légale (RGPD art. 6) |
|---|---|---|
| Créer et sécuriser votre compte, vous connecter | Téléphone, pays, session, appareil | Exécution du contrat |
| Fournir les actualités, la messagerie, les appels et les activités | Profil, contenus, messages, médias, données d'activité | Exécution du contrat |
| Ordonner votre fil d'actualités | Centres d'intérêt, mesures de lecture | Intérêt légitime (proposer un fil pertinent) ; vous pouvez ajuster vos centres d'intérêt à tout moment |
| Retrouver vos contacts déjà sur Central | Numéros du carnet | Consentement (permission du téléphone), retirable à tout moment |
| Choisir qui peut voir vos statuts | Correspondances entre comptes Central issues de votre carnet | Consentement (permission d'accès aux contacts), retirable à tout moment |
| Partager votre position dans une discussion | Latitude / longitude | Consentement (permission et geste explicite) |
| Ouvrir un compte de paiement | Identité, coordonnées, situation, justificatifs | Exécution du contrat (mesures précontractuelles) |
| Tenir le compte, exécuter les transferts, recharges et envois, émettre les reçus | Solde, opérations, bénéficiaires, IBAN, numéros Mobile Money | Exécution du contrat |
| Vérification d'identité et lutte contre le blanchiment | Identité, justificatifs, opérations | Obligation légale (Code monétaire et financier) |
| Vous envoyer des notifications | Identifiant de notification | Consentement (autorisation du téléphone) |
| Sécurité, prévention des abus et de la fraude | Adresse IP, journaux, appareils | Intérêt légitime (protéger le service et ses utilisateurs) |
| Répondre à vos demandes | E-mail, contenu de la demande | Exécution du contrat / intérêt légitime |

## 4. Destinataires, sous-traitants et partenaires

Vos données ne sont accessibles qu'aux personnes de Central qui en ont besoin, et aux prestataires suivants, chacun pour sa mission :

| Prestataire | Rôle | Données concernées | Localisation |
|---|---|---|---|
| Amazon Web Services (AWS) | Hébergement des serveurs, de la base de données et des fichiers | Toutes les données du service | Union européenne (Paris) |
| Google (Firebase Authentication avec reCAPTCHA, Firebase Cloud Messaging, serveur STUN de secours) | Vérification du numéro par SMS, notifications, établissement des appels en secours seulement | Téléphone, identifiant de notification, adresse IP, données techniques du navigateur pour reCAPTCHA | Monde, dont États-Unis |
| Apple (Apple Push Notification service) | Acheminement des notifications sur iPhone | Identifiant de notification, contenu de la notification | Monde, dont États-Unis |
| Apple (Plans / MapKit) — sur iPhone | Aperçu de carte et adresse d'une position partagée dans Coz | Coordonnées de la position partagée, adresse IP | Monde, dont États-Unis |
| Google (Google Maps : Maps SDK, géocodage) — sur Android | Aperçu de carte et adresse d'une position partagée dans Coz | Coordonnées de la position partagée, adresse IP | Monde, dont États-Unis |
| Swan (établissement de monnaie électronique agréé, France) | Compte de paiement en euros, IBAN, virements et vérification d'identité | Identité, coordonnées, situation, justificatifs, opérations | Union européenne |
| Stripe | Recharge du compte par carte bancaire | Données de carte (saisies chez Stripe), montant | Union européenne et États-Unis |
| pawaPay | Recharges et envois par Mobile Money | Numéro Mobile Money, montant, devise | Royaume-Uni, et pays de l'opérateur Mobile Money concerné (Afrique) |

Swan et Stripe agissent, pour leurs propres obligations réglementaires (vérification d'identité, lutte contre le blanchiment, prévention de la fraude), en tant que **responsables de traitement distincts** ; leurs politiques de confidentialité s'appliquent en complément de celle-ci. Les éditeurs de presse dont vous lisez les articles traitent les données de leur propre site sous leur seule responsabilité.

Chacun de ces prestataires encadre le traitement des données qui lui sont confiées par ses propres engagements contractuels de protection des données, publiés dans ses conditions de service. Nous pouvons aussi communiquer des données aux autorités lorsque la loi l'impose.

## 5. Transferts hors de l'Union européenne

Google, Apple et Stripe peuvent traiter des données aux États-Unis. Ces transferts sont encadrés par les garanties qu'offre chaque prestataire : son adhésion au Data Privacy Framework UE–États-Unis lorsqu'elle existe, ou les clauses contractuelles types adoptées par la Commission européenne, prévues dans ses conditions de traitement des données.

Les transferts vers pawaPay, au Royaume-Uni, s'appuient sur la décision d'adéquation de la Commission européenne pour le Royaume-Uni. Lorsque vous rechargez votre compte ou envoyez de l'argent par Mobile Money, les données nécessaires à l'opération (numéro de téléphone, montant, devise) sont transmises à l'opérateur Mobile Money du pays concerné, en Afrique ; ce transfert est nécessaire à l'exécution de l'opération que vous demandez (RGPD, art. 49.1.b).

## 6. Durées de conservation

| Données | Durée de conservation |
|---|---|
| Compte, profil et préférences | Pendant toute la durée du compte, puis suppression ou anonymisation dans un délai raisonnable après sa clôture |
| Messages, médias et historique d'appels | Pendant toute la durée du compte, ou jusqu'à leur suppression par l'utilisateur |
| Statuts Coz | 24 heures de visibilité |
| Mesures de lecture | Pendant toute la durée du compte |
| Identité, vérification, données d'ouverture de compte de paiement et opérations financières | 5 ans après la fin de la relation (obligation légale de lutte contre le blanchiment) |
| Pièces comptables | 10 ans (Code de commerce) |
| Identifiants de notification | Jusqu'à la déconnexion de l'appareil ou l'expiration de l'identifiant |
| Adresses IP de limitation des abus | Quelques minutes (fenêtre de limitation) |
| Journaux techniques | 12 mois au maximum |
| Numéros du carnet envoyés pour rapprochement | Non conservés : comparés aux comptes existants puis écartés une fois la réponse rendue |
| Correspondances de carnet (statuts) | Tant que le contact figure dans votre carnet ; supprimées à la suppression du compte |

## 7. Sécurité

- Les échanges entre l'application et nos serveurs sont chiffrés (HTTPS / TLS, WebSocket sécurisé).
- Le jeton de session est conservé dans le coffre sécurisé du téléphone ; le code de paiement n'est conservé que sous forme d'empreinte.
- Les fichiers (photos, documents) sont servis par des liens signés à durée limitée.
- Les secrets de nos serveurs sont conservés dans un coffre dédié, jamais dans le code.

En cas de violation de données présentant un risque pour vous, nous en informerons la CNIL dans les 72 heures et, si le risque est élevé, nous vous en informerons directement.

## 8. Vos droits

Conformément au RGPD et à la loi Informatique et Libertés, vous disposez des droits suivants :
- **accès** à vos données et obtention d'une copie ;
- **rectification** des données inexactes (la plupart se modifient directement dans l'application) ;
- **effacement**, dans les limites des obligations légales de conservation (notamment financières) ;
- **limitation** du traitement ;
- **portabilité** des données que vous nous avez fournies ;
- **opposition** aux traitements fondés sur notre intérêt légitime, dont l'ordonnancement de votre fil d'actualités ;
- **retrait de votre consentement** à tout moment (contacts, position, notifications) via les réglages du téléphone ;
- définir des **directives sur le sort de vos données après votre décès**.

Pour exercer ces droits, écrivez à **contact@centralworldapp.com** en indiquant le numéro de téléphone de votre compte. Nous pourrons vous demander de confirmer votre identité. Nous répondons dans un délai d'un mois, prolongeable de deux mois pour les demandes complexes.

**Suppression de votre compte :** la suppression n'est pas encore disponible dans l'application. Envoyez votre demande à **contact@centralworldapp.com** en indiquant le numéro de téléphone de votre compte. Elle est traitée sous 30 jours. Les données que la loi nous oblige à conserver (identité, opérations financières, pièces comptables) sont alors conservées, à accès restreint, pendant les durées indiquées à la section 6 ; le reste est supprimé ou anonymisé.

**Réclamation :** si vous estimez que vos droits ne sont pas respectés, vous pouvez saisir la Commission nationale de l'informatique et des libertés (CNIL), 3 place de Fontenoy, TSA 80715, 75334 Paris Cedex 07 — www.cnil.fr.

## 9. Mineurs

Central est réservé aux personnes âgées d'au moins **18 ans**, en raison de ses services financiers et de la vérification d'identité qu'ils exigent. Nous ne collectons pas sciemment de données concernant des mineurs ; si vous pensez qu'un mineur nous a transmis des données, écrivez à contact@centralworldapp.com.

## 10. Modifications

Cette politique sera mise à jour lorsque de nouvelles fonctions ouvriront. La date en tête de page indique la dernière version. En cas de changement important, nous vous en informerons dans l'application.
