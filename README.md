# 🩺 Mask Detector

## 🎯 Description
**Mask Detector** est une application Python qui utilise **OpenCV** et des classificateurs en cascade de Haar pour détecter les visages via la webcam et déterminer si une personne porte un masque ou non.

L’application utilise un flux vidéo en temps réel et distingue :
- 🟢 **Mask** : lorsqu’un visage est détecté mais la bouche n’est pas visible.  
- 🔴 **No Mask** : lorsqu’un visage et une bouche sont détectés dans la même région.  
- ⚪ **No face found...** : lorsqu’aucun visage n’est détecté.

---

## 🧩 Technologies utilisées
- **Python 3.7+**
- **OpenCV (opencv-python)**
- **Cascade Classifiers (fichiers XML fournis par OpenCV)**

---

## ⚙️ Installation

### 1️⃣ Crée un environnement virtuel (optionnel mais recommandé)
```bash
python -m venv .env
```
--- 

### Activation sous windows
.\.env\Scripts\activate

### Activation sous Linux/Mac
source .env/bin/activate

### Installation des dependances
pip install -r requirements.txt

### Lancement de l'application
python main.py
---

## Remarques importantes
- Assure-toi qu’aucune autre application n’utilise ta caméra avant d’exécuter le script.
- Si le programme affiche Erreur : impossible d’accéder à la caméra, essaye de changer :
```python
cap = cv2.VideoCapture(0)
```
en 

```python
cap = cv2.VideoCapture(1)
```
