# Changelog CleanMailbox Thunderbird Extension

Ce fichier résume les changements importants pour les **utilisateurs finaux** à partir de la version **0.11.0**.  
Les détails techniques et le journal complet restent dans `history.md`.

## 0.11.0 — 2026-02-26

- **Sécurité de la clé API clarifiée**
  - La manière dont la clé API CleanMailbox est stockée (en local dans Thunderbird) est désormais documentée de façon explicite.
  - Le README explique les risques en cas d’accès au profil Thunderbird et rappelle les bonnes pratiques (rotation/révocation de la clé via le manager CleanMailbox).
- **Documentation sécurité enrichie**
  - Nouvelle section « Sécurité — clé API » dans la documentation utilisateur.
  - Un document dédié (`.doc/security.md`) décrit plus en détail les décisions prises côté sécurité.
- **Protection renforcée contre les extensions malveillantes**
  - L’extension vérifie désormais que les messages internes proviennent bien d’elle-même avant de les traiter.
  - En pratique, cela réduit le risque qu’une autre extension tente d’abuser des actions de signalement ou de blacklist.
- **Déplacement automatique vers Indésirables**
  - Après « Signaler comme Spam » ou « Ajouter à la Blacklist », le message est désormais déplacé automatiquement dans le dossier **Indésirables**.
- **Interface du popup**
  - La police du popup est alignée sur celle de l’interface Thunderbird (même rendu que dans les paramètres).
- **Correctif déplacement vers Indésirables**
  - Correction d’une erreur lors du déplacement vers Indésirables (utilisation du dossier Junk réel du compte au lieu d’un dossier virtuel).

