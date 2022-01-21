# PID documentations

## A quoi sert un asservissement PID ?

Le rôle d'un algorithme de correction PID est d'améliorer 3 principales caractéristiques d'un système : la rapidité, la précision et la stabilité.

Pour un moteur par exemple, ces éléments se traduisent par une montée en régime rapide, une vitesse réelle très proche de celle demandée et un fonctionnement à la vitesse de consigne sans oscillations (accélérations, décélération...).

En quelques mots, le PID sert à réduire l'écart qu'il y a entre une valeur de consigne et la valeur mesurée. Dans notre exemple : l'erreur entre la vitesse effective d'un moteur et la consigne qu'il lui a été donnée.

Pour fonctionner le PID à donc besoin de plusieurs choses : un actionneur à asservir, un capteur pour mesurée la grandeur voulue et un organe de contrôle (microcontrôleur par exemple) capable de faire les calculs et d'interpréter les informations de consigne et du capteur.

La régulation a également besoin de 3 paramètres qui sont des coefficients à entrés par l'utilisateur. Un paramètre pour la régulation proportionnelle (Kp), intégrale (Ki), dérivée (Kd). Ces coefficients vont avoir une influence sur le comportement du système : il peut être rapide, lent, stable, oscillant, précis...

Ces coefficients sont à changer en fonction de chaque applications qui n'auront pas les même besoins mais aussi en fonction de chaque actionneur qui n'auront pas la même façon de se comporter pour un même triplet de paramètres.

Mais comment obtient on Kp, Ki, Kd ? La manière la plus simple est de le faire manuellement (par essais/erreurs) en changeant un paramètre à la fois !

Kp aura une influence sur la rapidité d'un moteur à atteindre sa vitesse de consigne, Ki réduira l'erreur statique (erreur entre la vitesse demandée et la vitesse mesurée) et Kd réduira les oscillations engendrées.


## Sources

* https://www.robot-maker.com/shop/blog/33_Asservir-moteurs-courant-continu-PID.html
* http://grauonline.de/alexwww/ardumower/pid/pid.html
* https://towardsdatascience.com/emulating-a-pid-controller-with-long-short-term-memory-part-1-bb5b87165b08
* https://www.mathworks.com/help/reinforcement-learning/ug/tune-pi-controller-using-td3.html
* https://www.mdpi.com/2076-3417/11/17/8002/pdf
* file:///tmp/mozilla_vorph0/applsci-11-08002-v2.pdf
* https://fr.wikipedia.org/wiki/Circuit_en_boucle_ouverte
* https://fr.wikipedia.org/wiki/Th%C3%A9orie_du_contr%C3%B4le
* https://arxiv.org/pdf/2006.05604.pdf
* https://medium.com/@maohar502/pid-tuning-using-machine-learning-6cf6f7fe5690