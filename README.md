# LAB4_
🧪 LAB 4 : Analyse statique d’un APK avec JADX GUI + dex2jar + JD-GUI

Cours : Sécurité des applications mobiles

1. 🔁 Rappel : Compilation Android

Une application Android est compilée comme suit :

Java/Kotlin → .class → .dex → APK
2. 📘 Vue d’ensemble

Ce lab consiste à analyser un APK sans l’exécuter (analyse statique) pour identifier :

code source
vulnérabilités
données sensibles
3. 🎯 Objectifs pédagogiques
Comprendre la structure d’un APK
Décompiler un APK
Identifier des failles simples
Comparer différents outils
4. ⚙️ Prérequis
JADX
JD-GUI
dex2jar
APK de test
5. 🔒 Règles de sécurité
Utiliser uniquement des APK de test
Ne pas analyser des apps réelles sensibles
Respecter l’éthique
6. 📘 Glossaire
APK : package Android
DEX : bytecode Android
JAR : archive Java
Reverse engineering : analyse du code
7. 🧰 Task 1 — Préparer workspace
Créer dossier lab4_apk
Copier APK
🔗 Capture 1 — Workspace

<img width="502" height="443" alt="1" src="https://github.com/user-attachments/assets/b8598f13-161d-4b35-aefc-17ab9fe5a0f4" />


8. 📥 Task 2 — Obtenir APK
Commande :
adb pull /data/app/app.apk


9. 🔍 Task 3 — Analyse avec JADX
Ouvrir APK dans JADX GUI


📌 Résultat :

code Java visible
10. 🔎 Task 4 — Recherche chaînes sensibles

Rechercher :

password
token
api_key


11. 🔄 Task 5 — dex2jar
Commande :
d2j-dex2jar.sh app.apk


12. 📊 Task 6 — Comparaison outils
Outil	Avantage	Limite
JADX	simple	code partiel
JD-GUI	lisible	moins Android
13. 📝 Task 7 — Mini-rapport

Inclure :

outil utilisé
vulnérabilités
observations
14. 🧹 Task 8 — Nettoyage
supprimer fichiers
fermer outils
15. ⚠️ Troubleshooting
APK non lisible → vérifier version
erreur dex2jar → vérifier Java
16. ✅ Deliverables
captures
analyse
rapport
17. 🎯 Bonus — Réponses guidées
Permissions excessives

Certaines apps demandent accès inutile (ex: GPS).

Composant exporté

Peut être exploité pour injecter intents.

URL en clair

Utiliser HTTPS + chiffrement.

Obfuscation

Cache code mais pas tout (strings visibles).

Token stockage

SharedPreferences = risqué (persistant).

allowBackup=true

Risque extraction données → mettre false.

exported=true

Accessible par apps externes.

WebView JS

Active risques XSS → limiter usage.
