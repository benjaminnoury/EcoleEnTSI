---
title: Écoles d'ingénieur recrutant des TSI
--- 


### Nota Bene

Cette liste des écoles est en **cours de construction** et à destination des cpge TSI. Les options non accessibles depuis une cpge TSI n'ont pas été répertoriées. Elle vise à être exhaustive mais en est encore loin. 
Elle est élaborée à partir d'informations glanées sur les plaquettes et sites des écoles ainsi que de l'expérience des élèves qui ont passé les concours d'entrée.

Si des informations vues sur les plaquettes ou sites des écoles sont contradictoires avec celles ci-dessous, préférer celles données directement par les écoles. Merci de me le faire savoir, pour que je mette à jour le tableau.



### Recherche

Vous pouvez faire une recherche sur toutes les entrées du tableau grâce à la boite de saisie ci-dessous.

Quelques exemples des possibilités :

- **Paris** vous donnera toutes les écoles de l'académie de Paris.
- **électronique** vous donnera toutes les écoles avec une filière électronique
- **insa rennes** vous donnera toutes les options de l'INSA de Rennes
- **polytech mécanique** vous donnera toutes les écoles du réseau polytech ayant une filière mécanique
- **apprentissage** vous donnera les filières par apprentissage de toutes les écoles.
- **CCP** vous donnera toutes les écoles du concours CCP et de la banque de note CCP


Il est également possible de changer le critère de tri des écoles ( par défaut, par ordre alphabétique des noms des écoles ) en cliquant sur les entêtes de colonne. 

:::maj
!bash
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
date +Mise\ à\ jour\ le\ %d\ %h\ à\ %H:%M
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
:::

!csv(Ecoles_TSI.csv)(Ecole|Académie|Ville|Spécialité|Type de recrutement|Informations complémentaires|Oral)


<script>$(document).ready(function() {
	$('#tableau_ecole').DataTable({
		"paging":	false,
		"info":		false		
		});
	});</script>
