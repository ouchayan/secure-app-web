# secure-app-web
Comment sécuriser une application web
- Authentification :
- Authorisation :
- Encryption : Encodes data so only authorized parties can decode it.
- error handling : Manages responses when things go wrong, avoiding revealing sensitive info.
- logging ands monitoring :
- token expired
- ip whitelisting : autoriser l'accés aux ip trusted.
- Systèmes de détection d'intrusion.
- WAF : Le pare-feu applicatif se place devant la couche présentation. Tous les flux applicatifs de type HTTP et HTTPS passent donc par lui avant d’accéder à la couche présentation de l’application.
Le filtrage se réalise de deux manières : soit par liste blanche, soit par liste noire.
- authentification forte.
- Rate limiting :spécifier le nombre d'appel par temps pour eviter la surcharge (20 appels par minute).
- Validation des entrées et nettoyage des données (Validation : Email, password, username Netyoyage : supprimer les balises HTML pour empêcher les attaques XSS, Échappez les caractères spéciaux, tels que <, > et &, pour empêcher les attaques par injection HTML. Utilisez des requêtes paramétrées ou des instructions préparées lors de l'interaction avec des bases de données pour empêcher les attaques par injection SQL. Cela implique l'utilisation d'espaces réservés pour la saisie utilisateur dans les requêtes SQL.

- HTML Tag Sanitization:

Sanitization: Use a library like Validator.js to remove HTML tags from user input to prevent XSS attacks. Example: validator.stripTags(input).
Escape Special Characters:

Sanitization: Escape special characters, such as <, >, and &, to prevent HTML injection attacks. Example: validator.escape(input).
Preventing SQL Injection:

Sanitization: Use parameterized queries or prepared statements when interacting with databases to prevent SQL injection attacks. This involves using placeholders for user input in SQL queries.
File Path Sanitization:

Sanitization: Ensure that file paths provided by users are valid and do not allow access to unintended directories or files.
Implementing strong input validation and sanitization practices is crucial for several reasons:
Preventing Security Vulnerabilities: Proper validation and sanitization help protect against common web vulnerabilities, such as cross-site scripting (XSS) and SQL injection, by ensuring that user input cannot be used to execute malicious code or manipulate databases.

Ensuring Data Integrity: Validating user input helps maintain data integrity by ensuring that only valid and expected data is processed or stored. It reduces the chances of errors or data corruption caused by invalid input.

Enhancing User Experience: By providing immediate feedback on invalid input, you can improve the user experience by guiding users to correct any mistakes or omissions.
Now, let's explore some best practices and examples of input validation and sanitization using JavaScript.
- 
