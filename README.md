# 🎓 Power BI – Système de Suivi Académique & Administratif  
**Dashboard complet : Étudiants · Absences · Notes · Recouvrement · Professeurs**

![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![PowerBI](https://img.shields.io/badge/Power%20BI-Data%20Analytics-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![GitHub](https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge)

---

## 📌 **Description du Projet**

Ce projet Power BI a pour objectif de fournir un **système décisionnel complet** destiné à la direction d’un établissement académique.  
Il permet de suivre :

- 📚 Les effectifs  
- 🕒 Les absences  
- 📝 Les notes et taux de réussite  
- 💰 Le recouvrement financier  
- 👨‍🏫 La charge des professeurs  

Le rapport est entièrement automatisé grâce à un **modèle en étoile** et des **mesures DAX professionnelles**.

---

## 📁 **Structure du Projet**

├── 📁 data/ # Fichiers sources Excel (étudiants, modules, absences, notes, etc.)
├── 📁 pbix/ # Fichiers Power BI Desktop
├── 📁 screenshots/ # Captures d’écran des dashboards
├── README.md # Documentation du projet
---

## 🧠 **Technologies utilisées**

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Power Query**
- **Modèle de données en étoile**
- **Excel**

---

## ⭐ **Fonctionnalités du Dashboard**

### 🔹 1. Suivi global (Dashboard Direction)
- Nombre total d’étudiants  
- Taux de réussite global  
- Taux d’absentéisme  
- Évolution des effectifs  
- Répartition par filière & niveau  

📸 *Capture d’écran :*  
`/screenshots/dashboard_direction.png`
<img width="644" height="351" alt="image" src="https://github.com/user-attachments/assets/ad3f1a27-6731-440e-92eb-cc34cdab44e2" />



---

### 🔹 2. Suivi des absences
- Heures d’absence par module  
- Taux d’absentéisme par groupe  
- Absences par étudiant  
- Analyse par professeur  

📸 *Capture d’écran :*  
`/screenshots/dashboard_absences.png`
<img width="722" height="425" alt="image" src="https://github.com/user-attachments/assets/1b3b4ac2-3e5d-46f5-9e55-3bb27cd048b7" />


---

### 🔹 3. Suivi pédagogique : Notes & Résultats
- Moyenne générale  
- Notes finales pondérées (CC, TP, Projet, Examen)  
- Taux de réussite par module  
- Classement des étudiants  

📸 *Capture d’écran :*  
`/screenshots/dashboard_notes.png`
<img width="695" height="381" alt="image" src="https://github.com/user-attachments/assets/04e15443-fb31-4df6-a068-9d5c44c54ac2" />

---

### 🔹 4. Recouvrement financier
- Montant facturé  
- Montant encaissé  
- Reste à payer  
- Taux de recouvrement  

📸 *Capture d’écran :*  
`/screenshots/dashboard_recouvrement.png`
<img width="698" height="391" alt="image" src="https://github.com/user-attachments/assets/2877df50-d476-4e45-babf-2be578d22243" />

---

### 🔹 5. Dashboard Professeurs
- Heures prévues vs réalisées  
- Charge d’enseignement  
- Répartition par module & groupe  

📸 *Capture d’écran :*  
`/screenshots/dashboard_professeurs_rh.png`
<img width="635" height="392" alt="image" src="https://github.com/user-attachments/assets/5ae11cab-eb24-42a3-bf85-e55325962e28" />

---

## 📊 **Modèle de données**

Modèle en étoile basé sur :

- **Dimensions** : Étudiant, Module, Professeur, Filière, Niveau, Groupe, Temps…
- **Tables de faits** : Notes, Absences, Recouvrement, ChargeEnseignement….


---

## 🧮 **Exemples de Mesures DAX**

### 🔹 Nombre d’étudiants
```DAX
Nb Etudiants = DISTINCTCOUNT(Dim_Etudiant[IdEtudiant])
🔹 Taux de réussite
Taux Reussite = DIVIDE([Nb Modules Valides], [Nb Modules Total])
🔹 Montant facturé
Montant Facture = SUM(F_Recouvrement[MontantFacture])

---

🚀 Installation & utilisation
1️⃣ Cloner le dépôt
    git clone https://github.com/votre_nom/votre_projet.git
2️⃣ Ouvrir le fichier
    pbix/rapport_powerbi.pbix
3️⃣ Mettre à jour les sources Excel si nécessaire
