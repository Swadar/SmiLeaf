# <p align="center">  🍀 SmiLeaf 🍀</p>

<img width="1280" height="720" alt="SmiLeaf" src="https://github.com/user-attachments/assets/0da974f6-0666-44fc-af05-1d88e940991f" />


<br>
<p align="center">SmiLeaf est un système de serre intelligente automatisée conçue pour optimiser la croissance des semis (particulièrement les radis) en simulant des conditions environnementales idéales grâce à l'informatique embarquée.</p>
<br>

# <p align="center">Les Principes :</p>

- **Arrosage Intelligent :** Surveillance de l'humidité du sol pour maintenir un substrat constant, crucial pour éviter que les radis ne deviennent fibreux.

- **Phototropisme Artificiel :** Rotation automatique de la plante via un servomoteur pour équilibrer l'exposition lumineuse et éviter que les tiges ne "filent".

- **Régulation Thermique :** Ventilation active pour maintenir une température fraîche (température idéale pour le radis < 22°C).

- **Interface Émotionnelle :** Affichage OLED/LCD indiquant les constantes (T°/H) et l'état de santé de la plante via des expressions faciales

<br>

# <p align="center">Le Matériel Requis :</p> 

* **Carte Arduino UCA (fabriquée par RFThings) incluant :**
    * <details>
        <summary>Capteur humidité et de température -> SHTC3</summary>
        <br>
        ▪ The SHTC3 is a low-cost, easy to use, highly accurate, digital temperature and humidity sensor.<br>
        ▪ I2C communication built-in your UCA board.<br>
        ▪ The sensor covers a humidity measurement range of 0 to 100 %RH and a temperature measurement range of -40 °C to 125 °C with a typical accuracy of ±2 %RH and ±0.2°C.
      </details>
    * <details>
        <summary>Capteur de luminosité -> LTR-303A</summary>
        <br>
        ▪ The LTR-303ALS-01 is a low voltage I2C digital light sensor in a low cost mount package.<br>
        ▪ I2C communication built-in your UCA board.<br>
        ▪ It provides a linear response over a wide dynamic range from 0.01 lux to 64k lux and is well suited to applications under high ambient brightness.
      </details>

<img width="1422" height="796" alt="board1" src="https://github.com/user-attachments/assets/61d95a37-e045-4c48-8715-7e27f906ec91" />

*  <details> <summary><strong>Capteur d'humidité dans le sol -> MSMS</strong></summary>  <br> ▪ Voltage : 2.5V - 7.0V <br> ▪ Sortie : Analogique (Inversée) <br> ▪ Sonde : Capacitive & Double face  <br> ▪ Extras : Port Grove, LED indicateurs, Mode économie d'énergie <br> ▪ https://www.cytron.io/p-maker-soil-moisture-sensor
  </details>

<img width="557" height="491" alt="Capteur humidité" src="https://github.com/user-attachments/assets/079f006c-81a5-42b8-b99d-447b00132030" />

* <details><summary><strong>Servo Moteur -> SG90 9G</strong></summary> <br> ▪ Modulation : Analogique <br> ▪ Force : 4.8V (1.6 kg-cm) <br> ▪ Vitesse : 4.8V (0.1 sec/60°) <br> ▪ Poids : 9g <br> ▪ Dimensions : 23mm x 12.2mm x 29mm <br> ▪ Angle de rotation : 180° <br> ▪ Connectique : Connecteur 3 points <br> ▪ https://boutique.semageek.com/fr/104-micro-servo-tower-pro-sg90-3007447379574.html
  </details>
<img width="368" height="368" alt="Servo" src="https://github.com/user-attachments/assets/65685276-d9d7-4c74-b270-fe2b25483cfe" />

* <details>
    <summary><strong>Ecran OLED</strong></summary><br> ▪ Taille : 1.3 inch <br> ▪ Résolution : 128  64 <br> ▪ Couleur d'affichage : Bleu <br> ▪ Driver : SSD1106 <br> ▪ Protocole : I2C communication Protocol <br> ▪ Dimensions du panneau : 34.5 * 23.0 * 1.4 (mm) <br> ▪ Zone active :** 29.42 * 14.7 (mm) <br> ▪ Température de fonctionnement : -30°C ~ 70°C <br> ▪ Compatibilité : Arduino (UNO R3), STM, Raspberry Pi, Beagle Bone Black <br> ▪ https://passionelectronique.fr/ecran-oled-i2c-arduino/
  </details>
<img width="100" height="100" alt="Ecran led" src="https://github.com/user-attachments/assets/793c50ce-27ca-4245-911d-579b8be72625" />

<br>

# <p align="center">L'installation :</p> 

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
 pi install https://github.com/Swadar/SmiLeaf
 ```

# <p align="center">Les Avancées :</p> 

# <p align="center">La Conception :</p> 

