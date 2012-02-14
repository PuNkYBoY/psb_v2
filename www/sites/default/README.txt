Après deux ou trois problèmes d'installation de Drupal sur mon ordinateur, j'ai décidé de faire ce fichier pour solutionner certains problèmes

== Problème de dossier temporaire ==
Si vous avez une erreur du type :
  failed to open stream: "DrupalTemporaryStreamWrapper::stream_open"
C'est que vous avez un problème au niveau de votre redirection sur votre dossier temporaire dans la section "admin/config/media/file-system" de votre Drupal.
 * Lien d'exemple : http://wstaw.org/m/2012/02/14/plasma-desktopiV1574.png

== Settings ==
Dans ce répertoire existe un fichier "default.settings.php", une fois renommé en "settings.php" il vous permet d'assigner une configuration à votre Drupal et surtout de définir votre base de donnée.
Comme vos informations sur votre base de donnée peuvent être différentes des autres, le fichier "settings.php" ne doit en aucun cas être versionné, seulement le défaut.
Vous pouvez tout de même vous en servir pour votre propre configuration.
Suite à ça vous devrez appliquer un chmod 440 (lecture seule) sur le fichier settings.php

 Merci de ne pas modifier les droits de ce dossier puisque ce répertoire ne devrait pas être accessible en écriture