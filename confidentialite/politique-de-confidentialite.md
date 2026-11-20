# Politique de confidentialité de Central

_Version bêta 1.0 — dernière mise à jour : 20 novembre 2026_

Central est actuellement en **version bêta**. Cette politique sera mise à jour à mesure que le service évolue, notamment lors de la création de la structure juridique qui l'exploitera.

Cette politique explique quelles données personnelles l'application Central (et ses services Cosam, Coz, Ecoz, Cozview, Activity et Hub) collecte, pourquoi, avec qui elles sont partagées, combien de temps elles sont gardées et comment exercer vos droits.

## 1. Responsable du traitement

Le responsable du traitement est **Résiste Rayll MAKITA MPIKA**, porteur du projet Central. La structure juridique qui exploitera Central est en cours de création ; dès sa constitution, elle deviendra responsable du traitement et cette politique sera mise à jour en conséquence.

- Contact pour toute question sur vos données et pour exercer vos droits : **contact@centralworldapp.com**

## 2. Les données que nous traitons

Nous ne collectons que ce qui sert un service que vous utilisez. Les accès sensibles du téléphone (contacts, position, micro, appareil photo, photos) ne sont demandés qu'au moment où vous utilisez la fonction concernée, et vous pouvez les refuser ou les retirer à tout moment dans les réglages du téléphone.

### 2.1 Compte et connexion
- Numéro de téléphone (identifiant de connexion) et pays du compte.
- Code de vérification reçu par SMS : il est envoyé et vérifié par Firebase Authentication (Google). Central reçoit le résultat de la vérification, pas le code.
- Jeton de session : stocké dans le trousseau sécurisé du téléphone (Keychain iOS / Keystore Android), jamais en clair.

### 2.2 Profil
- Nom affiché, prénom et nom déclarés, pseudo (@username) et sa visibilité, photo de profil, texte « à propos », adresse e-mail (facultative, jamais utilisée pour se connecter).
- Profils par service (Coz, Ecoz, Cozview, Activity, Hub) : nom et photo propres à chaque service si vous les définissez.
- Réglage « me trouver par mon numéro » (découvrabilité).

### 2.3 Identité et vérification (KYC)
Ces données ne sont demandées que pour les services qui l'exigent légalement (ouvrir un compte de paiement, déposer ou sortir de l'argent).
- État civil : prénom, nom, date de naissance, ville et pays de naissance, nationalité, adresse de résidence, e-mail.
- Pour l'ouverture d'un compte de paiement en euros : situation professionnelle, tranche de revenu mensuel et, lorsque la réglementation l'exige, numéro d'identification fiscale.
- Selon le service : pièce d'identité, selfie photo ou vidéo, permis de conduire, CV, certificats, photo professionnelle ou de créateur, que vous déposez dans « Mon dossier ».
- Pour un compte en euros, la vérification de votre identité est réalisée par notre partenaire bancaire Swan, sur ses propres pages ; c'est Swan qui rend la décision. Central conserve le statut de cette vérification.

### 2.4 Paiements et argent (Cosam)
- Comptes, soldes, opérations, bénéficiaires, motifs, devis de change, historique et reçus.
- IBAN de votre compte en euros (tenu par Swan) et IBAN des bénéficiaires que vous enregistrez.
- Numéro de Mobile Money utilisé pour une recharge ou un envoi.
- Carte bancaire : vos numéros de carte sont saisis directement dans le formulaire sécurisé de Stripe (pour une recharge par carte) ou gérés par Swan (pour une carte Central). **Central ne reçoit ni ne stocke jamais le numéro complet de votre carte.**
- Code secret Cosam : vérifié par nos serveurs pour autoriser une opération sensible.

### 2.5 Contacts du téléphone (Coz)
Si vous l'autorisez, Coz lit les numéros de votre carnet d'adresses et les envoie à nos serveurs pour savoir **lesquels correspondent à un compte Central**. Le serveur ne renvoie que les numéros trouvés et ne conserve pas votre carnet. Les noms de vos contacts ne sont pas envoyés.

### 2.6 Messagerie et appels (Coz)
- Contenu de vos messages, notes vocales, photos, vidéos, documents, sondages, réactions, statuts (visibles 24 heures) et informations de groupe. **Les messages ne sont pas chiffrés de bout en bout** : ils sont chiffrés pendant le transport (HTTPS / WSS) et stockés sur nos serveurs pour être remis à vos correspondants et synchronisés.
- Appels audio et vidéo : la communication passe directement entre les appareils (WebRTC). **Aucun appel n'est enregistré.** Pour établir la connexion, votre appareil interroge un serveur STUN de Google, qui voit votre adresse IP.
- Position : uniquement quand vous choisissez de partager votre position dans une discussion ; seul un point (latitude, longitude) est envoyé, sans suivi continu.
- Verrou de discussion : la reconnaissance Face ID / Touch ID / empreinte et le code du verrou restent sur votre appareil et ne sont jamais envoyés.
- Export de discussion : le fichier est créé à votre demande et vous choisissez où l'envoyer.

### 2.7 Contenus publiés (Ecoz, Cozview, Hub)
Publications, commentaires, abonnements et relations, vidéos et leurs miniatures, boutique, annonces et articles mis en vente. Ce que vous publiez publiquement est visible des autres utilisateurs.

### 2.8 Activités professionnelles (Activity)
Si vous gérez une activité (Immobilier, Flotte, Bar, Hôtel) : membres, rôles, locataires, contrats et baux, réservations, courses, recettes, documents et photos que vous y déposez. Vous êtes responsable des données de tiers (locataires, chauffeurs, clients) que vous y enregistrez.

### 2.9 Accueil et actualités
Vos centres d'intérêt et recherches d'actualités. Quand une recherche d'actualités est active, le texte de la requête est transmis par nos serveurs à Brave Search, **sans votre identité**. Un article ouvert dans le lecteur intégré est chargé depuis le site de l'éditeur, qui applique sa propre politique.

### 2.10 Données techniques
- Appareil : plateforme (iOS / Android / web), nom de l'appareil, jeton de notification, date de dernière activité.
- Adresse IP et identifiants de requête, utilisés dans les journaux techniques pour la sécurité et le diagnostic.
- Préférences locales (réglages d'affichage, cache) stockées sur votre appareil.

**Ce que nous ne faisons pas :** Central n'intègre aucun outil de mesure d'audience, de publicité ciblée, de suivi publicitaire ni de rapport de plantage tiers, et ne vend pas vos données.

## 3. Finalités et bases légales

| Finalité | Données | Base légale (RGPD art. 6) |
|---|---|---|
| Créer et sécuriser votre compte, vous connecter | Téléphone, pays, session, appareil | Exécution du contrat |
| Fournir la messagerie, les appels, les publications, les activités | Profil, messages, médias, contenus, données Activity | Exécution du contrat |
| Retrouver vos contacts déjà sur Central | Numéros du carnet | Consentement (permission du téléphone), retirable à tout moment |
| Partager votre position dans une discussion | Latitude / longitude | Consentement (permission et geste explicite) |
| Ouvrir et tenir un compte de paiement, exécuter les paiements, recharges et transferts | Identité, KYC, données de paiement | Exécution du contrat |
| Lutte contre le blanchiment et le financement du terrorisme, vérification d'identité | Identité, KYC, opérations | Obligation légale (Code monétaire et financier) |
| Vous envoyer des notifications | Jeton de notification | Exécution du contrat ; vous pouvez les désactiver dans le téléphone |
| Sécurité, prévention de la fraude, diagnostic | Adresse IP, journaux, appareil | Intérêt légitime (protéger le service et ses utilisateurs) |
| Répondre à vos demandes | E-mail, contenu de la demande | Exécution du contrat / intérêt légitime |

La pièce d'identité et le selfie peuvent contenir des données biométriques au sens du RGPD lorsqu'ils servent à vous identifier ; ce contrôle est réalisé par Swan, en application de ses obligations légales.

## 4. Destinataires, sous-traitants et partenaires

Vos données sont accessibles aux seules personnes de Central qui en ont besoin, et aux prestataires suivants, chacun pour sa mission :

| Prestataire | Rôle | Données concernées | Localisation |
|---|---|---|---|
| Amazon Web Services EMEA (AWS) | Hébergement des serveurs, de la base de données et des fichiers | Toutes les données du service | Union européenne (Paris, eu-west-3) |
| Google (Firebase Authentication, Firebase Cloud Messaging, serveur STUN) | Vérification du numéro par SMS, notifications Android, établissement des appels | Téléphone, jeton de notification, adresse IP | Monde, dont États-Unis |
| Apple (Apple Push Notification service) | Notifications et appels entrants sur iPhone | Jeton de notification, contenu de la notification | Monde, dont États-Unis |
| Swan (établissement de monnaie électronique agréé, France) | Compte de paiement en euros, IBAN, virements, cartes, vérification d'identité | Identité, KYC, opérations | Union européenne |
| Stripe | Recharge de votre compte par carte bancaire | Données de carte (saisies chez Stripe), montant | Union européenne et États-Unis |
| pawaPay | Recharges et envois par Mobile Money | Numéro Mobile Money, montant, référence | Royaume-Uni et pays de l'opérateur Mobile Money concerné (Afrique) |
| Brave Software | Recherche d'actualités | Texte de la requête, sans identité | États-Unis |

Swan et Stripe agissent, pour leurs propres obligations réglementaires (vérification d'identité, lutte anti-blanchiment, prévention de la fraude), en tant que **responsables de traitement distincts** ; leurs politiques de confidentialité s'appliquent en complément de celle-ci.

Nous pouvons aussi communiquer des données aux autorités lorsque la loi l'impose (autorités judiciaires, administratives, Tracfin).

Chacun de ces prestataires encadre le traitement des données qui lui sont confiées par ses propres engagements contractuels de protection des données, publiés dans ses conditions de service.

## 5. Transferts hors de l'Union européenne

Certains prestataires (Google, Apple, Stripe, Brave) peuvent traiter des données aux États-Unis. Ces transferts sont encadrés par les garanties qu'offre chaque prestataire : son adhésion au Data Privacy Framework UE–États-Unis lorsqu'elle existe, ou les clauses contractuelles types adoptées par la Commission européenne, prévues dans ses conditions de traitement des données.

Les transferts vers le Royaume-Uni (pawaPay) s'appuient sur la décision d'adéquation de la Commission européenne. Lorsque vous envoyez de l'argent vers un compte Mobile Money hors de l'UE, les données nécessaires à l'opération (numéro du bénéficiaire, montant) sont transmises à l'opérateur du pays de destination, ce qui est nécessaire à l'exécution de l'opération que vous demandez (RGPD art. 49.1.b).
## 6. Durées de conservation

| Données | Durée de conservation |
|---|---|
| Compte et profil | Pendant toute la durée du compte, puis suppression ou anonymisation dans un délai raisonnable après sa clôture |
| Messages et médias Coz | Tant que le compte est actif ou jusqu'à leur suppression par l'utilisateur |
| Statuts Coz | 24 heures de visibilité |
| Identité, KYC et opérations financières | 5 ans après la fin de la relation ou l'opération (obligation légale anti-blanchiment) |
| Pièces comptables | 10 ans (Code de commerce) |
| Jetons de notification | Jusqu'à la déconnexion de l'appareil ou l'expiration du jeton |
| Journaux techniques | 12 mois au maximum |
| Numéros du carnet envoyés pour rapprochement | Non conservés : ils sont comparés aux comptes existants puis écartés une fois la réponse rendue |

Les écritures du registre financier ne sont jamais effacées : une erreur est corrigée par une écriture inverse, ce qui garantit l'exactitude de l'historique exigée par la réglementation.

## 7. Sécurité

- Toutes les communications entre l'application et nos serveurs sont chiffrées (HTTPS / TLS, WebSocket sécurisé).
- Le jeton de session et le code du verrou de discussion sont stockés dans le coffre sécurisé du téléphone ; les données d'identité ne restent pas sur l'appareil après leur envoi.
- Les fichiers (photos, documents) sont servis par des liens signés à durée limitée.
- Les secrets de nos serveurs sont conservés dans un coffre dédié et jamais dans le code.
- Les opérations sensibles demandent votre code secret.

En cas de violation de données présentant un risque pour vous, nous en informerons la CNIL dans les 72 heures et, si le risque est élevé, nous vous en informerons directement.

## 8. Vos droits

Conformément au RGPD et à la loi Informatique et Libertés, vous disposez des droits suivants :
- **accès** à vos données et obtention d'une copie ;
- **rectification** des données inexactes (la plupart se modifient directement dans l'application) ;
- **effacement**, dans les limites des obligations légales de conservation (notamment financières) ;
- **limitation** du traitement ;
- **portabilité** des données que vous nous avez fournies (l'export d'une discussion Coz est disponible dans l'application) ;
- **opposition** aux traitements fondés sur notre intérêt légitime ;
- **retrait de votre consentement** à tout moment (contacts, position) via les réglages du téléphone ;
- définir des **directives sur le sort de vos données après votre décès**.

Pour exercer ces droits, écrivez à **contact@centralworldapp.com** en indiquant le numéro de téléphone de votre compte. Nous pourrons vous demander de confirmer votre identité. Nous répondons dans un délai d'un mois, prolongeable de deux mois pour les demandes complexes.

**Suppression de votre compte :** envoyez votre demande à **contact@centralworldapp.com** en indiquant le numéro de téléphone de votre compte. Elle est traitée sous 30 jours. Les données que la loi nous oblige à conserver (identité et opérations financières, pièces comptables) sont alors conservées, à accès restreint, pendant les durées indiquées à la section 6 ; le reste est supprimé ou anonymisé.

**Réclamation :** si vous estimez que vos droits ne sont pas respectés, vous pouvez saisir la Commission nationale de l'informatique et des libertés (CNIL), 3 place de Fontenoy, TSA 80715, 75334 Paris Cedex 07 — www.cnil.fr.

## 9. Mineurs

Central est réservé aux personnes âgées d'au moins **18 ans**, en raison de ses services financiers et de la vérification d'identité qu'ils exigent. Nous ne collectons pas sciemment de données concernant des mineurs ; si vous pensez qu'un mineur nous a transmis des données, écrivez à contact@centralworldapp.com.

## 10. Modifications

Nous pouvons mettre à jour cette politique. La date en tête de page indique la dernière version. En cas de changement important, nous vous en informerons dans l'application.
