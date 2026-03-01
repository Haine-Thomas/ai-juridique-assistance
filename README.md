# JurisConsult AI
## L'assistant juridique intelligent qui n'hallucine pas. 

### La Vision Produit (Le "Pourquoi")

  En France, 60% des dirigeants de TPE/PME hésitent à consulter un avocat pour des questions simples à cause du coût et de la complexité. Les LLMs classiques (ChatGPT, Claude) sont puissants mais présentent un risque majeur : l'hallucination juridique.
  
  JurisConsult AI résout ce problème en combinant la puissance de l'IA générative avec une base de connaissances juridique stricte et vérifiée.
  Valeur ajoutée :
  
  Fiabilité augmentée : Utilisation du RAG (Retrieval-Augmented Generation) pour forcer l'IA à citer ses sources (Code du Travail, Code de Commerce).
  
  Accessibilité : Traduction du jargon complexe en conseils actionnables pour un non-expert.
  
  Confidentialité : Approche "Privacy-First" dans le traitement des documents téléchargés.

### Architecture Technique & Choix "Product Engineer"

  Ce projet n'est pas qu'un wrapper d'API. Chaque choix technique répond à un impératif métier :
  
  Frontend & Fullstack : Next.js 15 avec App Router et Server Actions pour une performance optimale et un SEO maîtrisé.
  
  Moteur d'IA : Intégration du Vercel AI SDK pour une gestion fluide du streaming des réponses (UX "Real-time").
  
  Recherche Sémantique (RAG) : * Vector DB : Pinecone (ou Supabase Vector) pour stocker les embeddings.
  
  Embeddings : text-embedding-3-small d'OpenAI pour un rapport coût/précision optimal.
  
  Validation de Données : Zod pour garantir que les inputs utilisateurs et les réponses de l'IA respectent un schéma strict.
  
  UI/UX : Tailwind CSS + Shadcn/UI pour une interface sobre, professionnelle et rassurante (codes visuels du secteur légal).

### Fonctionnalités Clés

  Analyse de Documents : Upload de contrats (PDF/Docx) et extraction automatique des clauses à risque.
  
  Chat Contextuel : Posez des questions sur votre propre document ou sur le droit général.
  
  Sourcing Automatique : Chaque réponse est accompagnée d'un lien vers l'article de loi ou la section du document source.
  
  Mode Hors-Ligne (Draft) : Sauvegarde locale des consultations pour une reprise rapide.

### Ce que j'ai appris (Le regard "Dev")

  Gestion des Hallucinations : Mise en place d'un système de System Prompt rigoureux et de filtres post-génération.
  
  Optimisation des Coûts : Implémentation d'un cache pour les requêtes fréquentes afin de réduire la consommation de tokens OpenAI.
  
  Parsing de PDF complexes : Gestion des tableaux et des mises en page multi-colonnes souvent présentes dans les textes de loi.

### Installation (Local Dev)

  Cloner le projet
  Bash

  git clone https://github.com/Haine-Thomas/ai-juridique-assistance.git

  Installer les dépendances
  Bash

  npm install

  Variables d'environnement
  Créez un fichier .env.local :
  Extrait de code

  OPENAI_API_KEY=votre_cle
  PINECONE_API_KEY=votre_cle
  DATABASE_URL=votre_url_db

  Lancer le serveur
  Bash

  npm run dev

👨‍💻 À propos

Je suis Thomas Haine, Développeur Fullstack JS avec une forte culture Product Engineer. J'aime construire des outils qui automatisent l'expertise humaine sans la remplacer.
