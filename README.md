<div align="center">
  <img src="assets/hero.png" alt="Agentic BI Hero Image" width="100%" />
</div>

<p align="center">
  <b><a href="#english">🇬🇧 English</a> | <a href="#ελληνικά">🇬🇷 Ελληνικά</a></b>
</p>

---

<h1 id="english">🇬🇧 Agentic BI - HR Analytics (English)</h1>

**Description:** This repository is an educational template demonstrating how to use Agentic AI (like GitHub Copilot Chat in Agent mode) to autonomously build a Power BI semantic model and custom HTML KPI cards for an HR Analytics scenario.

## 🔍 What is Agentic Development?

Agentic development is a new paradigm where developers shift from writing code or using UI applications to guiding intelligent agents. The developer defines the what - the requirements, rules, and intent - and the AI agent handles the how - generating specs, implementing the model, running validations, fixing issues, and iterating toward a working solution. 

In Power BI, this is made possible by open file formats with [Power BI Project file format](https://learn.microsoft.com/power-bi/developer/projects/projects-overview) and the [TMDL language](https://learn.microsoft.com/analysis-services/tmdl/tmdl-overview), which provide structure and linting AI agents can use to reason, check, and improve their own work. 

## ⚙️ How does it work?

1. You describe what you need – your [requirements](.requirements/requirements-01.md) and the [rules](.resources/kb-pbip.md) the agent should follow.
2. An AI agent turns that into a development spec – readable, reviewable, and adjustable.
3. You say "Go" and the agent starts implementing the spec autonomously.
4. It runs its own best practice checks, fixes issues, and iterates until it gets it right.
5. You open the Power BI application and review the result, just like you would with a teammate’s pull request.

## 🧪 Example Included

This repository comes with an HR Analytics example, tracking active employees, turnover rate, and training hours based on an HR data warehouse schema. Check the `.requirements` folder for the details.

## 🚀 Try it yourself

1. Clone this Repo into your laptop
2. Install [Visual Studio Code](https://code.visualstudio.com/)
3. Install [GitHub Copilot extension](https://docs.github.com/en/copilot/responsible-use-of-github-copilot-features/responsible-use-of-github-copilot-chat-in-your-ide?tool=vscode)
4. Open Github Copilot Chat in [Agent mode](https://code.visualstudio.com/blogs/2025/02/24/introducing-copilot-agent-mode)
5. Attach the [requirements-01.md](.requirements/requirements-01.md) and run the following prompt:

    > Please review the attached requirements and draft a comprehensive development specification in Markdown format for my review.

6. Review the generated development spec, then prompt Copilot to proceed with implementing the semantic model.

> 💡 **Notes** 
> - The [kb-pbip.md](.resources/kb-pbip.md) file includes important knowledge base that AI will use to better understand PBIP file structure and TMDL.
> - The [kb-html-cards.md](.resources/kb-html-cards.md) file contains instructions for generating custom HTML KPI Cards.
> - Best results are usually achieved using advanced models like `Claude 3.5 Sonnet` or `Gemini`.

## 🤝 Credits & Mentions
This project was inspired by and builds upon the excellent work of others in the Power BI community:
- **[Rui Romano](https://github.com/RuiRomano)**: For the original [pbip-demo-agentic](https://github.com/RuiRomano/pbip-demo-agentic) repository which provided the foundational Agentic AI workflow for Power BI.
- **YouTube Community**: For the insights on using AI (like Claude) to generate HTML Viewer DAX code for custom KPI cards (see [Claude Just Replaced My Power BI KPI Cards](https://www.youtube.com/watch?v=KV84OuB5q_4)).

---

<h1 id="ελληνικά">🇬🇷 Agentic BI - HR Analytics (Ελληνικά)</h1>

**Περιγραφή:** Αυτό το repository αποτελεί ένα εκπαιδευτικό πρότυπο που δείχνει πώς να χρησιμοποιήσετε την τεχνολογία Agentic AI (όπως το GitHub Copilot Chat σε Agent mode) για να δημιουργήσετε αυτόνομα ένα μοντέλο δεδομένων (semantic model) στο Power BI και προσαρμοσμένες κάρτες HTML KPI, εστιασμένο στον τομέα του Ανθρώπινου Δυναμικού (HR Analytics).

## 🔍 Τι είναι η Ανάπτυξη με Agentic AI;

Η Ανάπτυξη με Agent (Agentic Development) είναι ένα νέο μοντέλο όπου οι προγραμματιστές δεν γράφουν κώδικα ούτε χρησιμοποιούν εφαρμογές με γραφικό περιβάλλον (UI), αλλά **καθοδηγούν έξυπνους AI agents**. Ο προγραμματιστής ορίζει το *«τι»* (τις απαιτήσεις, τους κανόνες και τον σκοπό) και ο AI agent αναλαμβάνει το *«πώς»* – παράγει προδιαγραφές, υλοποιεί το μοντέλο, τρέχει ελέγχους, διορθώνει προβλήματα και βελτιώνεται μέχρι να παραδώσει μια λειτουργική λύση.

Στο Power BI, αυτό γίνεται εφικτό χάρη στα ανοιχτά πρότυπα αρχείων, όπως το [Power BI Project file format (.pbip)](https://learn.microsoft.com/power-bi/developer/projects/projects-overview) και η [γλώσσα TMDL](https://learn.microsoft.com/analysis-services/tmdl/tmdl-overview). Αυτά προσφέρουν τη δομή που χρειάζεται η Τεχνητή Νοημοσύνη για να «διαβάζει» τον κώδικα, να ελέγχει τα λάθη της και να αυτοβελτιώνεται.

## ⚙️ Πώς λειτουργεί;

1. Περιγράφετε αυτό που χρειάζεστε – δηλαδή τις [απαιτήσεις](.requirements/requirements-01.md) και τους [κανόνες](.resources/kb-pbip.md) που πρέπει να ακολουθήσει το AI.
2. Ο AI agent μετατρέπει τις οδηγίες σε ένα **αναλυτικό πλάνο υλοποίησης**, το οποίο μπορείτε να διαβάσετε και να διορθώσετε.
3. Δίνετε το «πράσινο φως» ("Go") και ο agent ξεκινά την υλοποίηση εντελώς αυτόνομα.
4. Ο agent ελέγχει μόνος του τον κώδικά του, διορθώνει τυχόν σφάλματα (bugs) και επαναλαμβάνει τη διαδικασία μέχρι το αποτέλεσμα να είναι σωστό.
5. Ανοίγετε την εφαρμογή Power BI και ελέγχετε το τελικό αποτέλεσμα, σαν να ελέγχατε τη δουλειά ενός συνεργάτη σας!

## 🧪 Το Παράδειγμα του Repository

Αυτό το repository περιέχει ένα έτοιμο παράδειγμα για **HR Analytics**. Ο στόχος του AI είναι να παρακολουθεί τους ενεργούς υπαλλήλους, το ποσοστό αποχωρήσεων (turnover rate) και τις ώρες εκπαίδευσης, με βάση μια εικονική βάση δεδομένων (HR data warehouse). Δείτε τον φάκελο `.requirements` για όλες τις λεπτομέρειες.

## 🚀 Δοκιμάστε το μόνοι σας

1. Κατεβάστε (Clone) αυτό το Repo στον υπολογιστή σας.
2. Εγκαταστήστε το [Visual Studio Code](https://code.visualstudio.com/).
3. Εγκαταστήστε το [GitHub Copilot extension](https://docs.github.com/en/copilot/responsible-use-of-github-copilot-features/responsible-use-of-github-copilot-chat-in-your-ide?tool=vscode).
4. Ανοίξτε το Github Copilot Chat σε [Agent mode](https://code.visualstudio.com/blogs/2025/02/24/introducing-copilot-agent-mode).
5. Επισυνάψτε (Attach) το αρχείο [requirements-01.md](.requirements/requirements-01.md) στο Chat και γράψτε την εξής εντολή (prompt):

    > Please review the attached requirements and draft a comprehensive development specification in Markdown format for my review.

6. Διαβάστε το πλάνο υλοποίησης που θα σας δώσει το Copilot και έπειτα ζητήστε του να προχωρήσει με τη δημιουργία του Semantic Model!

> 💡 **Σημειώσεις**
> - Το αρχείο [kb-pbip.md](.resources/kb-pbip.md) είναι μια βάση γνώσεων. Το AI το διαβάζει για να μάθει πώς ακριβώς να συντάσσει αρχεία PBIP και TMDL.
> - Το αρχείο [kb-html-cards.md](.resources/kb-html-cards.md) περιέχει οδηγίες για τη δημιουργία πανέμορφων, προσαρμοσμένων **HTML KPI Cards** (όπως εξηγείται και σε σχετικά tutorials).
> - Τα καλύτερα αποτελέσματα επιτυγχάνονται με προηγμένα AI μοντέλα (π.χ. `Claude 3.5 Sonnet` μέσω Copilot Pro ή `Gemini`).

## 🤝 Αναφορές & Ευχαριστίες (Credits & Mentions)
Αυτό το έργο δημιουργήθηκε για εκπαιδευτικούς σκοπούς, αντλώντας έμπνευση από την εξαιρετική δουλειά της κοινότητας του Power BI:
- **[Rui Romano](https://github.com/RuiRomano)**: Για το αρχικό repository [pbip-demo-agentic](https://github.com/RuiRomano/pbip-demo-agentic) που παρείχε τη βασική αρχιτεκτονική του Agentic AI workflow για το Power BI.
- **YouTube Community**: Για την καινοτόμα ιδέα χρήσης του AI για τη δημιουργία custom KPI καρτών μέσω του HTML Viewer με χρήση DAX (βλ. το βίντεο [Claude Just Replaced My Power BI KPI Cards](https://www.youtube.com/watch?v=KV84OuB5q_4)).
