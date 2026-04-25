\# Agent Communication MIA



\## Objectif



Automatiser la création de contenus hebdomadaires pour les clients MIA :

article de blog, post Facebook et post Instagram, à partir d'un sujet 

choisi par le client.



\## Flux de fonctionnement



1\. Le client remplit un formulaire sur l'interface web (Vercel)

2\. Les données arrivent automatiquement dans Airtable

3\. Make.com déclenche une demande de création de contenu à Claude

4\. Claude génère les trois contenus (blog, Facebook, Instagram)

5\. Le client valide les contenus

6\. Une fois validés, les contenus sont envoyés sur les réseaux



\## Outils utilisés



\- Interface web : Vercel (formulaire client)

\- Base de données : Airtable

\- Automatisation : Make.com

\- Génération de contenu : Claude (Anthropic)



\## Points d'attention



\- Le client doit valider dans les 7 jours

\- Sans validation, la génération de la semaine est perdue

\- Les contenus modifiés par le client sont publiés sous sa responsabilité



\## Statut



✅ En production

## Flux visuel

```mermaid
flowchart TD
    A[🖥️ Client remplit le formulaire] --> B[📊 Données envoyées dans Airtable]
    B --> C[⚙️ Make.com déclenche l'automatisation]
    C --> D[🤖 Claude génère les contenus]
    D --> E[Blog + Facebook + Instagram]
    E --> F[👀 Client valide les contenus]
    F -->|✅ Validé| G[📤 Publication sur les réseaux]
    F -->|❌ Non validé sous 7 jours| H[🗄️ Dossier classé]
