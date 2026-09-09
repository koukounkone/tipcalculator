# Tip Calculator 📱💰

Une application Android moderne développée avec **Jetpack Compose** permettant de calculer facilement le pourboire lors d'une note de restaurant ou de service.

## 🚀 Fonctionnalités

- **Calcul dynamique :** Calcule en temps réel le montant du pourboire en fonction du montant de l'addition et du pourcentage saisi.
- **Option d'arrondi :** Possibilité d'arrondir le montant du pourboire à l'entier supérieur via un interrupteur (`Switch`).
- **Formataion de devise :** Formate automatiquement le résultat dans la monnaie locale (ex: `$10.00`, `10,00 €`).
- **Saisie personnalisée :**
  - Champ pour le montant de la facture (`Bill Amount`).
  - Champ pour le pourcentage de pourboire (`Service Rating`).
- **Interface responsive & accessible :**
  - Clavier adapté aux chiffres (`KeyboardType.Number`).
  - Actions clavier fluides (`ImeAction.Next` et `ImeAction.Done`).
  - Support du défilement vertical (`verticalScroll`).

---

## 🛠️ Technologies & Bibliothèques

- **Langage :** [Kotlin](https://kotlinlang.org/)
- **UI Framework :** [Jetpack Compose](https://developer.android.com/jetpack/compose) (Material 3)
- **Composants clés :**
  - `TextField` avec icône personnalisée
  - `Switch` interactif
  - `Column` / `Row` pour la mise en page
  - `remember` & `mutableStateOf` pour la gestion de l'état UI

---

## 🏗️ Structure du Code

Le fichier principal (`MainActivity.kt`) contient :

- **`MainActivity`** : Point d'entrée de l'application configuré avec `enableEdgeToEdge()`.
- **`TipTimeLayout`** : Composable principal gérant l'état (`amountInput`, `tipInput`, `roundUp`) et affichant l'interface utilisateur.
- **`calculateTip`** : Fonction utilitaire privée calculant et formatant le montant selon la locale.
- **`EditNumberField`** : Reusable Composable pour la saisie de texte numérique avec icône contextuelle.
- **`RoundTheTipRow`** : Composant de ligne pour activer/désactiver l'arrondi du pourboire.
- **`TipTimeLayoutPreview`** : Fonction de prévisualisation Android Studio.

---

## 📋 Prérequis & Installation

1. **Android Studio** (Version Jellyfish ou supérieure recommandée).
2. **JDK 17** ou supérieur.
3. **Min SDK :** Android 7.0 (API level 24) ou supérieur.

### Étapes :
1. Clonez le dépôt ou importez le projet dans Android Studio.
2. Assurez-vous d'avoir les ressources suivantes dans votre dossier `res/` :
   - **Strings (`res/values/strings.xml`) :** `calculate_tip`, `bill_amount`, `how_was_the_service`, `round_up_tip`, `tip_amount`.
   - **Drawables (`res/drawable/`) :** `money.xml`, `percent.xml`.
3. Lancez l'application sur un émulateur ou un appareil physique.
