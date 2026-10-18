# email.thepunchlines.app

Pages publiques liées depuis les emails de Punchlines, servies par GitHub Pages.

- `desinscription.html` : désinscription des emails. Le lien de l'email appelle la fonction
  edge `unsubscribe` (dépôt JeSuis), qui redirige ici avec `?token=…&lang=fr|en` sans rien
  changer. La page montre le bouton « Me désinscrire », qui envoie `confirmer=1` en POST à
  la fonction ; elle désabonne puis revient ici avec `?statut=ok|invalide|erreur&lang=fr|en`.
  Un scanner de liens qui ouvre le lien ne désinscrit donc personne.

Pourquoi un sous-domaine à part : Supabase sert en `text/plain` toute page HTML renvoyée
par une fonction sur `*.supabase.co`, et l'app réclame tous les chemins de
`thepunchlines.app` (liens universels iOS, App Links Android). Une page posée là ouvrirait
l'app au lieu du navigateur sur un téléphone où elle est installée.
