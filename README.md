![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Arduino](https://img.shields.io/badge/-Arduino-00979D?style=for-the-badge&logo=Arduino&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Status](https://img.shields.io/badge/Statut-En%20D%C3%A9veloppement-orange?style=for-the-badge)

# <p align="center">  🍀 SmiLeaf 🍀</p>

<img width="1280" height="720" alt="SmiLeaf" src="https://github.com/user-attachments/assets/0da974f6-0666-44fc-af05-1d88e940991f" />


<br>
<p align="center">SmiLeaf est un système de serre intelligente automatisée conçue pour optimiser la croissance des semis (particulièrement les radis) en simulant des conditions environnementales idéales grâce à l'informatique embarquée.</p>
<br>

## 📖 Sommaire
1. [🌠 Les Principes](#les-principes-)
2. [Le Matériel Requis 🧰](#le-matériel-requis-)
3. [L'installation ⚙️](#linstallation-)
4. [Les Avancées 📈](#les-avancées-)
5. [La Conception ✏️](#la-conception-)
6. [Licence](#licence-)
---

## <p align="center">🌠Les Principes :</p>

- **Arrosage Intelligent :** Surveillance de l'humidité du sol pour maintenir un substrat constant, crucial pour éviter que les radis ne deviennent fibreux.

- **Phototropisme Artificiel :** Rotation automatique de la plante via un servomoteur pour équilibrer l'exposition lumineuse et éviter que les tiges ne "filent".

- **Régulation Thermique :** Ventilation active pour maintenir une température fraîche (température idéale pour le radis < 22°C).

- **Interface Émotionnelle :** Affichage OLED/LCD indiquant les constantes (T°/H) et l'état de santé de la plante via des expressions faciales

<br>

## <p align="center">🧰Le Matériel Requis :</p>

* **Carte Arduino UCA (fabriquée par RFThings) incluant :**
    * <details>
        <summary>🌡️ Capteur humidité et de température -> SHTC3</summary>
        <br>
        ▪ The SHTC3 is a low-cost, easy to use, highly accurate, digital temperature and humidity sensor.<br>
        ▪ I2C communication built-in your UCA board.<br>
        ▪ The sensor covers a humidity measurement range of 0 to 100 %RH and a temperature measurement range of -40 °C to 125 °C with a typical accuracy of ±2 %RH and ±0.2°C.
       <br>
        ▪ Utilité : Mesurer la température et l'humidité dans la serre afin de réguler ces deux paramètres avec une double porte. 
      </details>
    * <details>
        <summary>💡 Capteur de luminosité -> LTR-303A</summary>
        <br>
        ▪ The LTR-303ALS-01 is a low voltage I2C digital light sensor in a low cost mount package.<br>
        ▪ I2C communication built-in your UCA board.<br>
        ▪ It provides a linear response over a wide dynamic range from 0.01 lux to 64k lux and is well suited to applications under high ambient brightness.
       <br>
        ▪ Utilité : Mesurer la luminosité afin d'orienter une platforme sur laquelle se trouve la serre. 
      </details>

<img width="1422" height="796" alt="board1" src="https://github.com/user-attachments/assets/61d95a37-e045-4c48-8715-7e27f906ec91" />

*  <details> <summary><strong>💧 Capteur d'humidité dans le sol -> MSMS</strong></summary>  <br> ▪ Voltage : 2.5V - 7.0V <br> ▪ Sortie : Analogique (Inversée) <br> ▪ Sonde : Capacitive & Double face  <br> ▪ Extras : Port Grove, LED indicateurs, Mode économie d'énergie <br> ▪ https://www.cytron.io/p-maker-soil-moisture-sensor <br> ▪ Utilité : Mesurer l'humidité dans le sol afin d'arroser au moment le plus judicieux. <br> ▪ Image : <img width="557" height="491" alt="Capteur humidité" src="https://github.com/user-attachments/assets/079f006c-81a5-42b8-b99d-447b00132030" />
  </details>

* <details><summary><strong>⚙️ Servo Moteur -> SG90 9G</strong></summary> <br> ▪ Modulation : Analogique <br> ▪ Force : 4.8V (1.6 kg-cm) <br> ▪ Vitesse : 4.8V (0.1 sec/60°) <br> ▪ Poids : 9g <br> ▪ Dimensions : 23mm x 12.2mm x 29mm <br> ▪ Angle de rotation : 180° <br> ▪ Connectique : Connecteur 3 points <br> ▪ Utilité : double utilité, orienter la serre ainsi que d'ouvrir des fenêtre pour réguler la température et l'humidité. <br> ▪ https://boutique.semageek.com/fr/104-micro-servo-tower-pro-sg90-3007447379574.html <br> ▪ Image : <img width="368" height="368" alt="Servo" src="https://github.com/user-attachments/assets/65685276-d9d7-4c74-b270-fe2b25483cfe" />
  </details>

* <details>
    <summary><strong>📺 Ecran OLED</strong></summary><br> ▪ Taille : 1.3 inch <br> ▪ Résolution : 128  64 <br> ▪ Couleur d'affichage : Bleu <br> ▪ Driver : SSD1106 <br> ▪ Protocole : I2C communication Protocol <br> ▪ Dimensions du panneau : 34.5 * 23.0 * 1.4 (mm) <br> ▪ Zone active :** 29.42 * 14.7 (mm) <br> ▪ Température de fonctionnement : -30°C ~ 70°C <br> ▪ Compatibilité : Arduino (UNO R3), STM, Raspberry Pi, Beagle Bone Black <br> ▪ Utilité : Afficher les paramètres liés à la serre ainsi que d'afficher l'état de la plante. <br> ▪ https://passionelectronique.fr/ecran-oled-i2c-arduino/ <br> ▪ Image : <img width="100" height="100" alt="Ecran led" src="https://github.com/user-attachments/assets/793c50ce-27ca-4245-911d-579b8be72625" />
  </details>

* <details>
    <summary><strong>🚿 Pompe péristalrique ->  Kamoer NKP </strong></summary><br> ▪ Couleur : bleue <br> ▪ Source d'alimentation : DC power supply <br> ▪ Poids de l'article : 97,5 Grammes <br> ▪ Débit maximal : 70 Millilitres par minute <br> ▪ Tension : 12 Volts <br> ▪ Utilité : Arroser la plante. <br> ▪https://www.amazon.fr/p%C3%A9ristaltique-liquide-aquarium-laboratoire-analytique/dp/B0CHYKS1FZ/ref=asc_df_B0CHYKS1FZ?mcid=500d1304006a338b847f6bdd538a3818&tag=googshopfr-21&linkCode=df0&hvadid=701517366868&hvpos=&hvnetw=g&hvrand=12617936717180452031&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9109562&hvtargid=pla-2324789129714&psc=1&hvocijid=12617936717180452031-B0CHYKS1FZ-&hvexpln=0 <br> ▪ Image : <img width="461" height="591" alt="pompe " src="https://github.com/user-attachments/assets/56906f39-fdf3-444a-8696-b6ab045e0c10" />
  </details>


<br>

## <p align="center">⚙️L'installation :</p> 

* **USB Driver :** <br>
The board is using CH340C chip for USB. You may need to install the driver to use the board: https://sparks.gogo.co.nz/ch340.html

* **Board Programming - Board Manager :** <br>
 1. [Download and install the Arduino IDE](https://www.arduino.cc/en/Main/Software) (at least version v1.6.8)
 2. Start the Arduino IDE
 3. Go into Preferences
  Add 
 ```
 https://rfthings.github.io/ArduinoBoardManagerJSON/package_rfthings-avr_index.json
 ```
 as an "Additional Board Manager URL"
 
 4. Open the Boards Manager from the Tools -> Board menu and install "RFTHings AVR Boards by RFThings Vietnam"
 5. Select your RFTHings UCA board from the Tools -> Board menu
 6. Select Board version "3.9 and newer : AT328PB" from the Tools -> Board menu
 7. Select the port

* **Libraries :** <br>
Install libraries 
 ```
 git clone https://github.com/Swadar/SmiLeaf.git
 ```

## <p align="center">📈Les Avancées :</p> 

| **Etapes** | **Contributeurs** | **Etat : 🔴 (Pas commencé), 🟡 (En cours), 🟢 (Terminé)** | **Etat en %** |
| :--- | :--- | :---: | :---: |
| Arrosage intelligent | Nouhai Esteban | 🟡 | 50% |
| Phototropisme artificiel | Kamal Nicolas | 🟡 | 25% |
| Régulation thermique | Kamal Nicolas | 🟡 | 25% |
| Interface émotionnelle | Nouhai Esteban | 🟢 | 100% |
| Conception physique | Nouhai | 🟡 | 50% |
| Page Github | Esteban | 🟡 | 75% |
| Préparation orale | Nouhai Esteban Nico Kamal | 🔴 | 0% |

## <p align="center">✏️La Conception :</p> 
* <details><summary><strong> Première maquette :</strong></summary> <br> ▪ Méthode Employée : Dessin sur freeform <br> ▪ Schéma : <img width="1320" height="1639" alt="IMG_8903" src="https://github.com/user-attachments/assets/7f525a27-3afb-4dd6-98c8-877626cdb20e" /> 
  </details>
* <details><summary><strong> Deuxième maquette :</strong></summary> <br> ▪ Méthode Employée : Dessin sur freeform <br> ▪ Schéma : <img width="660" height="714" alt="Maquette 2" src="https://github.com/user-attachments/assets/6575dfff-a0db-4601-94e5-a5b520b79ee5" />
  </details>
* <details><summary><strong> Maquette Google Sketchup :</strong></summary> <br> ▪ Méthode Employée : Maquette 3D sur logiciel Sketchup <br> ▪ Lien : https://app.sketchup.com/share/tc/europe/1_Btm9EXOVA?source=web&stoken=UgGIBwFQeMK_y7TfFzfkmEnLTFg2cDbj6zdHrLS0E0Jew6M8zhHpEPFG9Bc530nx <br> ▪ Image : <img width="3440" height="1279" alt="Serre connectée" src="https://github.com/user-attachments/assets/f79b6f68-d238-4371-9158-67b41635abb3" /> 
  </details>



## <p align="center">Licence :</p> 

Le projet est réalisé dans le cadre de l'UE de communication sans fil du spatial au terrestre. 
<br> 
<img width="1287" height="800" alt="UCA_logo" src="https://github.com/user-attachments/assets/fe5291f9-ba6a-4fd3-a2ac-a5b69e7b7557" />


