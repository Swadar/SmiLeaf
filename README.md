# <p align="center">  🍀 SmiLeaf 🍀</p>
<img width="1379" height="752" alt="SmiLeaf" src="https://github.com/user-attachments/assets/67f4cec5-48b6-4634-bc4e-e0d314f29c69" />

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

*  <details> <summary><strong>Capteur d'humidité dans le sol -> MSMS</strong></summary> <br> ▪ https://www.cytron.io/p-maker-soil-moisture-sensor <br> ▪ Voltage : 2.5V - 7.0V <br> ▪ Sortie : Analogique (Inversée) <br> ▪ Sonde : Capacitive & Double face  <br> ▪ Extras : Port Grove, LED indicateurs, Mode économie d'énergie
  </details>

<img width="557" height="491" alt="Capteur humidité" src="https://github.com/user-attachments/assets/079f006c-81a5-42b8-b99d-447b00132030" />

- Servo Moteur
- Ecran LED

