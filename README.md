# email.thepunchlines.app

Pages publiques liées depuis les emails de Punchlines, servies par GitHub Pages.

- `desinscription.html` : confirmation de désinscription. La fonction edge `unsubscribe`
  (dépôt JeSuis) désabonne puis redirige ici avec `?statut=ok|invalide|erreur&lang=fr|en`.

Pourquoi un sous-domaine à part : Supabase sert en `text/plain` toute page HTML renvoyée
par une fonction sur `*.supabase.co`, et l'app réclame tous les chemins de
`thepunchlines.app` (liens universels iOS, App Links Android). Une page posée là ouvrirait
l'app au lieu du navigateur sur un téléphone où elle est installée.
