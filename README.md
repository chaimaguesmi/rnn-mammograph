# 🏥 Projet RNN - Classification de Mammographies

## 📌 Description
Projet de classification d'images mammographiques utilisant un réseau de neurones multi-tâches (détection et classification) sur le dataset MIAS.

---

## 🚀 Installation et Exécution

### Option 1 : Exécution sur Google Colab (Recommandé)

1. **Ouvrir le notebook dans Colab**
   - Cliquez sur ce lien : [![Open In Colab](https://colab.research.google.com/drive/1gAwNNqrAg8P1OZe86wnaPNHCzXYYYQH2?usp=sharing)]
   - Ou uploadez manuellement `RNN_Pretraitement.ipynb` sur Colab

2. **Le notebook téléchargera automatiquement les données**
   - Les données seront téléchargées depuis ce repository GitHub
   - Aucune configuration supplémentaire nécessaire !

3. **Exécuter toutes les cellules**
   - Menu → Runtime → Run all

---

### Option 2 : Exécution Locale

#### Prérequis
- Python 3.8+
- GPU recommandé (ou CPU avec patience 😄)

#### Installation

```bash
# Cloner le repository
git clone https://github.com/VOTRE_USERNAME/VOTRE_REPO.git
cd VOTRE_REPO

# Installer les dépendances
pip install -r requirements.txt

# Lancer Jupyter
jupyter notebook RNN_Pretraitement.ipynb
```

---

## 📂 Structure du Projet

```
.
├── RNN_Pretraitement.ipynb    # Notebook principal
├── README.md                   # Ce fichier
├── requirements.txt            # Dépendances Python
├── setup_data.py              # Script pour télécharger les données
├── dataset/                    # Dossier des données (généré automatiquement)
│   ├── Info.txt               # Métadonnées des images
│   ├── all-mias/              # Images mammographiques
│   └── info_labeled.csv       # Dataset labelisé
└── docs/
    └── INSTRUCTIONS.md        # Instructions détaillées
```

---

## 📊 Dataset

**MIAS Database (Mammographic Image Analysis Society)**
- **Source** : [MIAS Database](http://peipa.essex.ac.uk/info/mias.html)
- **Images** : 330 mammographies
- **Classes** :
  - Normal (N) : Images sans anomalie
  - Bénin (B) : Tumeurs bénignes
  - Malin (M) : Tumeurs malignes

---

## 🧠 Architecture du Modèle

### Multi-Task Learning
1. **Détection** : Présence/absence d'anomalie (binaire)
2. **Classification** : Type d'anomalie (Normal/Bénin/Malin)

### Backbone
- **ResNet50** pré-entraîné sur ImageNet
- Fine-tuning en 2 phases
- Augmentation de données

---

## 📈 Résultats Attendus

Le modèle devrait atteindre :
- **AUC-ROC Détection** : ~0.85-0.90
- **Accuracy Classification** : ~0.75-0.85

---



### Exécution Rapide (5 minutes)
1. Ouvrir le notebook dans Google Colab (lien ci-dessus)
2. Cliquer sur "Runtime" → "Run all"
3. Le notebook s'exécute automatiquement avec les données

---

## 📝 Auteur

**Votre Nom**
- Email : Chaima.guesmi@telecom-sudparis.eu
          ferdaoues.jaoued@telecom-sudparis.eu
- Date : 16 Février 2026

---


## 🙏 Remerciements

- Dataset MIAS
- TensorFlow/Keras
- Google Colab
