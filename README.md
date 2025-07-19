# Bot Discord OSINT

Un bot Discord avancé pour l'intelligence open source (OSINT) avec des commandes slash interactives.

## 🚀 Fonctionnalités

### Commandes disponibles:

- `/whois <domain>` - Recherche WHOIS complète sur un domaine
- `/geoip <ip>` - Géolocalisation d'adresse IP avec détails ISP
- `/phone <number>` - Analyse de numéro de téléphone (format international)
- `/dns <domain> [type]` - Requêtes DNS (A, MX, TXT, NS, CNAME, etc.)
- `/subdomain <domain>` - Énumération de sous-domaines
- `/email <email>` - Analyse d'adresse email et validation
- `/metadata <image_url>` - Extraction de métadonnées d'images

## 📋 Prérequis

- Python 3.8+
- Un bot Discord configuré
- Token Discord Bot

## 🛠️ Installation

1. **Cloner le projet**
```bash
git clone <repository_url>
cd discord-osint-bot
```

2. **Installer les dépendances**
```bash
pip install -r requirements.txt
```

3. **Configuration**
```bash
cp .env.example .env
# Éditer .env avec votre token Discord
```

4. **Lancer le bot**
```bash
python bot.py
```

## 🔧 Configuration Discord

### Créer un bot Discord:

1. Aller sur https://discord.com/developers/applications
2. Créer une nouvelle application
3. Aller dans "Bot" et créer un bot
4. Copier le token dans `.env`
5. Activer les intents nécessaires:
   - Message Content Intent
   - Server Members Intent (optionnel)

### Inviter le bot:

URL d'invitation avec permissions nécessaires:
```
https://discord.com/api/oauth2/authorize?client_id=YOUR_BOT_ID&permissions=2048&scope=bot%20applications.commands
```

Permissions requises:
- Send Messages
- Use Slash Commands
- Embed Links

## 📖 Utilisation

### Exemples de commandes:

```
/whois google.com
/geoip 8.8.8.8
/phone +33123456789
/dns example.com MX
/subdomain github.com
/email test@gmail.com
/metadata https://example.com/image.jpg
```

## 🔒 Sécurité et Éthique

⚠️ **Important**: Ce bot est destiné à des fins éducatives et de recherche légale uniquement.

### Règles d'utilisation:
- Respecter les lois locales et internationales
- Ne pas utiliser pour du harcèlement ou des activités malveillantes
- Obtenir l'autorisation avant d'analyser des domaines/IPs tiers
- Respecter les conditions d'utilisation des APIs externes

### Limitations:
- Certaines requêtes peuvent être limitées par les APIs gratuites
- Les résultats peuvent varier selon la disponibilité des données
- Pas de garantie sur l'exactitude des informations

## 🛡️ APIs Utilisées

- **ip-api.com**: Géolocalisation IP (gratuit, limité)
- **DNS publics**: Requêtes DNS standard
- **WHOIS**: Bases de données publiques
- **Phonenumbers**: Validation et analyse de numéros

## 🔄 Mises à jour

Le bot inclut un système de synchronisation automatique des commandes slash au démarrage.

## 📝 Logs

Les erreurs et événements sont loggés dans la console. Pour un logging avancé:

```python
import logging
logging.basicConfig(level=logging.INFO)
```

## 🤝 Contribution

Les contributions sont les bienvenues! Merci de:
1. Fork le projet
2. Créer une branche feature
3. Commit vos changements
4. Ouvrir une Pull Request

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.

## ⚠️ Disclaimer

Ce bot est fourni "tel quel" sans garantie. L'utilisation est sous votre responsabilité.
