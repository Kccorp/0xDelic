# 0xDelic
Ce challenge est orienté réseau et crypto. Il consiste a trouver le flag en analysant des trames réseau puis déchiffrer la chaine grâce aux indices données 

## Scénario

J'ai capturé le traffic internet de mon rival mathématicien Beaufort. Je sais qu'il prépare un sale coup, il a toujours le nez fouré dans ses algorithme. Je vais le devancer et voler en espérant trouver quelque chose.


Download : sample.pcapng

## Writ-up
La premiere étape est de comprendre qu'il faut regarder en priorité les requets dns et surtout les sous domain requeté

apres analyse et compréhension, nous repérons le domaine *.test.fr qui agit bizarrement et si nous relevons tous les sous domaine dans l'ordre nous obtenons : GBQUC62VKFDF6YTHMZUWWM3VPU======

Cette chaine finissant par des ==== nous fais penser a de la base, nous le passons donc dans cyberchef en mode magic pour le déchiffrer sois en base 32 nous obtenons :
0aA{UQF_bgfik3u}


il y a encore quelque chose qui ne va pas, le flag ne veut rien dire et le préfix 0xD{ n'est pas le bon. 
Comme dis dans l'énoncé, nous utiliserons l'algorithme de Beaufort pour décoder ce flag. 

Par déductions, sur le site https://dcode.fr/beaufort-cipher nous allons utiliser le mot 0xD comme clé de déchiffrement et nous obtenons donc le flag complet : 0xD{DNS_crypt3d}


![image](https://github.com/Kccorp/0xDelic/assets/85285247/a4a28add-5a83-4d8c-8b26-427ef6425a25)




![image](https://github.com/Kccorp/0xDelic/assets/85285247/6e874fe1-4d27-440f-be6c-7a519f89b1da)


