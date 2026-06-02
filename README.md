# 🌟 Mon Assistant Magique des Phrases

> Une application web interactive et ludique pour aider les enfants (à partir de 8 ans) à apprendre la structure des phrases, le vocabulaire et la grammaire française — spécialement conçue pour les enfants avec un léger retard de langage.

---

## 📖 Table des matières

- [Aperçu](#-aperçu)
- [Fonctionnalités](#-fonctionnalités)
- [Modes de jeu](#-modes-de-jeu)
- [Installation](#-installation)
- [Utilisation](#-utilisation)
- [Structure du projet](#-structure-du-projet)
- [Personnalisation](#-personnalisation)
- [Accessibilité](#-accessibilité)
- [Technologies](#-technologies)
- [Licence](#-licence)

---

## 🎯 Aperçu

**Mon Assistant Magique des Phrases** est une application HTML/CSS/JavaScript autonome qui fonctionne entièrement dans le navigateur, sans serveur ni connexion Internet requise après le premier chargement.

L'application propose un environnement coloré, bienveillant et motivant où l'enfant progresse à son rythme grâce à des exercices variés, un système de récompenses visuelles (étoiles, confettis) et une assistance vocale intégrée.

---

## ✨ Fonctionnalités

| Fonctionnalité | Description |
|----------------|-------------|
| 🔊 **Lecture vocale** | Toutes les instructions et phrases se lisent à voix haute en français pour faciliter la compréhension |
| 💡 **Aide contextuelle** | Bouton d'indices adaptés au niveau de l'enfant, accessible à tout moment |
| ⭐ **Système de récompenses** | Gagne des étoiles à chaque bonne réponse, avec animations de confettis |
| 🤖 **Mascotte bienveillante** | Un robot amical qui guide et encourage l'enfant tout au long du parcours |
| 📊 **Progression visuelle** | Barre de progression pour visualiser l'avancement dans chaque niveau |
| 🎨 **Design enfantin** | Couleurs vives, polices grandes (Comic Neue), animations douces et non stressantes |
| 📱 **Responsive** | Fonctionne sur ordinateur, tablette et smartphone |
| 🔄 **Rejouabilité** | Les mots sont mélangés aléatoirement à chaque partie pour éviter la mémorisation mécanique |

---

## 🎮 Modes de jeu

### 🧩 Remets dans l'ordre
L'enfant doit cliquer sur des mots mélangés pour les remettre dans le bon ordre et former une phrase correcte.

**Objectif pédagogique** : Comprendre la structure Sujet → Verbe → Complément.

### ✏️ Complète la phrase
Un mot est manquant dans la phrase. L'enfant doit le trouver parmi plusieurs propositions ou l'écrire.

**Objectif pédagogique** : Enrichir le vocabulaire et comprendre les accords (singulier/pluriel, masculin/féminin).

### 🔍 Trouve l'erreur
Une phrase contient une faute (accord, pluriel, structure). L'enfant doit l'identifier parmi plusieurs choix.

**Objectif pédagogique** : Développer l'attention portée à la grammaire et à l'orthographe.

### 🏗️ Construis ta phrase
L'enfant dispose d'un ensemble de mots et doit construire sa propre phrase grammaticalement correcte.

**Objectif pédagogique** : Stimuler la créativité linguistique et l'autonomie dans la production de phrases.

---

## 🚀 Installation

### Méthode 1 : Ouverture directe (recommandée)
1. Télécharge le fichier `assistant_phrases_enfant.html`
2. Double-clique dessus ou fais un clic droit → **Ouvrir avec** → Ton navigateur préféré

### Méthode 2 : Hébergement local
```bash
# Clone ou télécharge le projet
cd mon-assistant-phrases

# Ouvre dans le navigateur
open assistant_phrases_enfant.html        # macOS
xdg-open assistant_phrases_enfant.html    # Linux
start assistant_phrases_enfant.html       # Windows
```

### Méthode 3 : Serveur local (pour développement)
```bash
# Avec Python
python -m http.server 8000

# Avec Node.js (npx)
npx serve .

# Puis ouvre http://localhost:8000
```

> ⚠️ **Note** : La synthèse vocale nécessite une interaction utilisateur initiale (clic sur la page) sur certains navigateurs modernes pour des raisons de sécurité.

---

## 🕹️ Utilisation

1. **Choisis un mode de jeu** en cliquant sur une des 4 cartes colorées
2. **Écoute l'instruction** en cliquant sur le bouton 🔊 (lecture vocale)
3. **Réponds à l'exercice** :
   - **Mode ordre** : Clique sur les mots dans le bon ordre
   - **Mode complète** : Choisis ou écris le mot manquant
   - **Mode erreur** : Clique sur la bonne réponse
   - **Mode construis** : Clique sur les mots pour former ta phrase
4. **Vérifie ta réponse** avec le bouton ✅
5. **Demande de l'aide** 💡 si tu es bloqué
6. **Passe à l'exercice suivant** ➡️ quand c'est juste !

---

## 📁 Structure du projet

```
mon-assistant-phrases/
├── assistant_phrases_enfant.html    # Application complète (HTML/CSS/JS)
├── README.md                        # Ce fichier
└── LICENSE                          # Licence MIT
```

> L'application est volontairement contenue dans un seul fichier HTML pour faciliter le partage et l'utilisation sans dépendances externes.

---

## 🎨 Personnalisation

### Ajouter de nouveaux exercices

Ouvre le fichier HTML et modifie l'objet `exercises` dans la balise `<script>` :

```javascript
const exercises = {
    order: [
        {
            instruction: "Ton instruction personnalisée",
            words: ["mot1", "mot2", "mot3"],
            correct: ["mot1", "mot2", "mot3"],
            hint: "Un indice pour aider l'enfant",
            sentence: "La phrase complète à lire à voix haute."
        }
        // Ajoute d'autres exercices ici...
    ],
    complete: [ /* ... */ ],
    identify: [ /* ... */ ],
    build: [ /* ... */ ]
};
```

### Modifier les couleurs

Dans la section `<style>`, change les variables CSS `--primary`, `--secondary`, `--accent`, etc.

### Changer la voix

La synthèse vocale utilise les voix du système. Sur Windows, macOS et Linux, la voix française par défaut est automatiquement sélectionnée. Tu peux ajuster la vitesse (`rate`) et la hauteur (`pitch`) dans la fonction `speakText()`.

---

## ♿ Accessibilité

L'application intègre plusieurs fonctionnalités d'accessibilité :

- **Lecture vocale intégrée** pour les enfants en difficulté de lecture
- **Polices larges et lisibles** (Comic Neue, taille minimum 1.2rem)
- **Contraste élevé** entre le texte et le fond
- **Boutons larges** faciles à cliquer (adaptés aux écrans tactiles)
- **Animations douces** sans flash ni mouvements brusques
- **Messages d'erreur bienveillants** jamais punitifs
- **Support clavier** pour le mode "Complète la phrase" (touche Entrée)

---

## 🛠️ Technologies

- **HTML5** — Structure sémantique
- **CSS3** — Variables CSS, Flexbox, Grid, animations @keyframes
- **Vanilla JavaScript** — Aucune dépendance externe
- **Web Speech API** — Synthèse vocale native du navigateur
- **Google Fonts** — Police Comic Neue (chargée en ligne, mais l'app fonctionne sans)

### Compatibilité navigateurs

| Navigateur | Support |
|------------|---------|
| Chrome / Edge | ✅ Complet |
| Firefox | ✅ Complet |
| Safari | ✅ Complet (synthèse vocale légèrement différente) |
| Chrome Android | ✅ Complet |
| Safari iOS | ✅ Complet |

---

## 👥 Public cible

- Enfants de **7 à 10 ans**
- Enfants avec un **léger retard de langage**
- Enfants en **difficulté d'apprentissage** (dyslexie, TDAH)
- **Orthophonistes** et **éducateurs** en recherche d'outils ludiques
- **Parents** souhaitant accompagner leur enfant à la maison

---

## 🙏 Remerciements

- Police [Comic Neue](https://github.com/crozynski/comicneue) par Craig Rozynski
- Emojis open source pour la mascotte et les récompenses
- La communauté éducative pour les retours sur les besoins des enfants

---

## 📬 Contact & Contributions

Les contributions sont les bienvenues ! Si tu souhaites :
- Ajouter de nouveaux exercices
- Améliorer l'accessibilité
- Traduire l'application
- Signaler un bug

N'hésite pas à ouvrir une *issue* ou une *pull request*.

---

## 📄 Licence

Ce projet est sous licence **MIT** — voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

<p align="center">
  ⭐ Fais briller les étoiles de ton enfant ! ⭐
</p>
