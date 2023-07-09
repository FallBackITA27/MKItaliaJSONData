# MKItaliaJSONData
This is a backup of data in JSON format, so that it's accessible for anyone even when the site is down. Might not always be up to date.

The files can be accessed through the https://raw.githubusercontent.com/FallBackITA27/MKItaliaJSONData/main/ URL. All the URLs listed below are its subdomains.

# Documentation
* [User Documentation](#user)
* [MKW Documentation](#mkw)
    * [Raw Data](#mkw-raw)
    * [Sorted Data](#mkw-sorted)
        * [By Track](#mkw-by-track)
        * [By Player](#mkw-by-player)

## User
* player_id
    * Signed 32bit Integer
    * Holds the user id. It's One-based, there's no id 0.
* player_name
    * String
    * Holds the user's username. Maximum 25 Characters.
* region_id
    * Signed 32bit Integer (Can NULL)
    * Holds the user's region.
        * Refer to this JSON
        ```json
        {
            "0":  "Unknown",
            "2":  "Lazio",
            "3":  "Valle d'Aosta",
            "4":  "Piemonte",
            "5":  "Liguria",
            "6":  "Lombardia",
            "7":  "Trentino-Alto Adige",
            "8":  "Veneto",
            "9":  "Friuli-Venezia Giulia",
            "10": "Emilia-Romagna",
            "11": "Toscana",
            "12": "Umbria",
            "13": "Marche",
            "14": "Abruzzo",
            "15": "Molise",
            "16": "Campania",
            "17": "Puglia",
            "18": "Basilicata",
            "19": "Calabria",
            "20": "Sicilia",
            "21": "Sardegna"
        }
        ```
* province_id
    * Signed 32bit Integer (Can NULL)
    * Holds the user's region.
        * Refer to this JSON
        ```json
        {
            "0": {
                "0": "Sconosciuta"
            },
            "2": {
                "0": "Sconosciuta",
                "1": "Frosinone",
                "2": "Latina",
                "3": "Rieti",
                "4": "Roma",
                "5": "Viterbo"
            },
            "3": {
                "0": "Sconosciuta",
                "1": "Aosta"
            },
            "4": {
                "0": "Sconosciuta",
                "1": "Alessandria",
                "2": "Asti",
                "3": "Biella",
                "4": "Cuneo",
                "5": "Novara",
                "6": "Torino",
                "7": "Verbano-Cusio-Ossola",
                "8": "Vercelli"
            },
            "5": {
                "0": "Sconosciuta",
                "1": "Genova",
                "2": "Imperia",
                "3": "La Spezia",
                "4": "Savona"
            },
            "6": {
                "0": "Sconosciuta",
                "1": "Bergamo",
                "2": "Brescia",
                "3": "Como",
                "4": "Cremona",
                "5": "Lecco",
                "6": "Lodi",
                "7": "Mantova",
                "8": "Milano",
                "9": "Monza-Brianza",
                "10": "Pavia",
                "11": "Sondrio",
                "12": "Varese"
            },
            "7": {
                "0": "Sconosciuta",
                "1": "Sud Tirol",
                "2": "Trento"
            },
            "8": {
                "0": "Sconosciuta",
                "1": "Belluno",
                "2": "Padova",
                "3": "Rovigo",
                "4": "Treviso",
                "5": "Venezia",
                "6": "Verona",
                "7": "Vicenza"
            },
            "9": {
                "0": "Sconosciuta",
                "1": "Gorizia",
                "2": "Pordenone",
                "3": "Trieste",
                "4": "Udine"
            },
            "10": {
                "0": "Sconosciuta",
                "1": "Bologna",
                "2": "Ferrara",
                "3": "ForlÃ¬-Cesena",
                "4": "Modena",
                "5": "Parma",
                "6": "Piacenza",
                "7": "Ravenna",
                "8": "Reggio Emilia",
                "9": "Rimini"
            },
            "11": {
                "0": "Sconosciuta",
                "1": "Arezzo",
                "2": "Firenze",
                "3": "Grosseto",
                "4": "Livorno",
                "5": "Lucca",
                "6": "Massa Carrara",
                "7": "Pisa",
                "8": "Pistoia",
                "9": "Prato",
                "10": "Siena"
            },
            "12": {
                "0": "Sconosciuta",
                "1": "Perugia",
                "2": "Terni"
            },
            "13": {
                "0": "Sconosciuta",
                "1": "Ancona",
                "2": "Ascoli Piceno",
                "3": "Fermo",
                "4": "Macerata",
                "5": "Pesaro-Urbino"
            },
            "14": {
                "0": "Sconosciuta",
                "1": "Chieti",
                "2": "L'Aquila",
                "3": "Pescara",
                "4": "Teramo"
            },
            "15": {
                "0": "Sconosciuta",
                "1": "Campobasso",
                "2": "Isernia"
            },
            "16": {
                "0": "Sconosciuta",
                "1": "Avellino",
                "2": "Benevento",
                "3": "Caserta",
                "4": "Napoli",
                "5": "Salerno"
            },
            "17": {
                "0": "Sconosciuta",
                "1": "Bari",
                "2": "Barletta-Andria-Trani",
                "3": "Brindisi",
                "4": "Foggia",
                "5": "Lecce",
                "6": "Taranto"
            },
            "18": {
                "0": "Sconosciuta",
                "1": "Matera",
                "2": "Potenza"
            },
            "19": {
                "0": "Sconosciuta",
                "1": "Catanzaro",
                "2": "Cosenza",
                "3": "Crotone",
                "4": "Reggio Calabria",
                "5": "Vibo Valentia"
            },
            "20": {
                "0": "Sconosciuta",
                "1": "Agrigento",
                "2": "Caltanissetta",
                "3": "Catania",
                "4": "Enna",
                "5": "Messina",
                "6": "Palermo",
                "7": "Ragusa",
                "8": "Siracusa",
                "9": "Trapani"
            },
            "21": {
                "0": "Sconosciuta",
                "1": "Cagliari",
                "2": "Nuoro",
                "3": "Oristano",
                "4": "Sassari",
                "5": "Sud Sardegna"
            }
        }
        ```
* age
    * Signed 32bit Integer (Can NULL)
    * Holds the user's age.
* date_of_birth
    * String (Can NULL)
    * Date of the run stored in "yyyy-mm-dd" format.
* sex
    * bool (Can NULL)
    * Flag that indicates if the player is female.
* mii_data
    * String (Can NULL)
    * Mii data used for the run.
        * This is used for rendering miis. You can render these by using https://studio.mii.nintendo.com/miis/image.png?data=:mii_data&type=face&expression=normal&width=512&bgColor=FFFFFF00&clothesColor=default&cameraXRotate=0&cameraYRotate=335&cameraZRotate=0&characterXRotate=0&characterYRotate=0&characterZRotate=0&lightDirectionMode=none&instanceCount=1&instanceRotationMode=model
        * Example:
        
        ![Alt text](https://studio.mii.nintendo.com/miis/image.png?data=000f165d65747e849da0abafb5b7bab4bdbec4cbd3dae6ed040d141b1a2146404b52574a504a4961737b828c93988f&type=face&expression=normal&width=128&bgColor=FFFFFF00&clothesColor=default&cameraXRotate=0&cameraYRotate=335&cameraZRotate=0&characterXRotate=0&characterYRotate=0&characterZRotate=0&lightDirectionMode=none&instanceCount=1&instanceRotationMode=model)
* mixed
    * bool
    * Holds whether the player is mixed.
* country
    * String (Can NULL)
    * Only 3 Letters. Holds ID for Country.
* youtube
    * String (Can NULL)
    * Holds user's ID on the platform. Max 70 characters.
* twitch
    * String (Can NULL)
    * Holds user's ID on the platform. Max 70 characters.
* instagram
    * String (Can NULL)
    * Holds user's ID on the platform. Max 70 characters.
* twitter
    * String (Can NULL)
    * Holds user's ID on the platform. Max 70 characters.
* discord_id
    * Signed 64bit Integer (Can NULL)
    * Holds user's ID on discord.
## MKW
Here's the data:
* player_id
    * [Refer to User](#user)
* time
    * Signed 32bit Integer
    * the time on the track stored in milliseconds.
* track
    * Signed 16bit Integer
    * Stores the track it's on.
        * 0 - 31 Matching Tracks.
* category
    * Signed 16bit Integer
    * Stores the category it's on.
        * Refer to this JSON
        ```json
        {
            "0": "Normal",
            "1": "Shortcut",
            "2": "Glitch"
        }
        ``` 
* proof_status
    * Signed 16bit Integer
    * Stores the proof's status.
        * Refer to this JSON
        ```json
        {
            "0": "No Proof",
            "1": "To Be Announced",
            "2": "Photo",
            "3": "Video",
            "4": "Revolution Kart Ghost Data (RKG File)",
            "5": "Chadsoft Ghost",
        }
        ``` 
* is_pb
    * bool
    * Indicates if time is a PB.
* is_flap
    * bool
    * Indicates if time is a flap.
* is_200cc
    * bool
    * Indicates if time is played in 200cc.
* mii_name
    * String (Can NULL)
    * Mii name used for the run.
* mii_data
    * [Refer to User](#user)
* proof
    * String (Can NULL)
    * Holds a link to whatever type of proof.
        * If "proof_status" = 5, Proof is link to the RKG File on Chadsoft Servers
        * If "proof_status" = 4, Proof is link to the RKG File
        * If "proof_status" = 3, Proof is link to the video.
        * If "proof_status" = 2, Proof is link to the photo.
        * If "proof_status" = 1, Proof is null.
        * If "proof_status" = 0, Proof is null.
* video
    * String (Can NULL)
    * Link to a recording of the run.
        * This is the same as "proof" if "proof_status" = 4.
* character
    * Signed 16bit Integer (Can NULL)
    * Character ID according to [Tockdom.com](https://wiki.tockdom.com/wiki/List_of_Identifiers#Characters)
* vehicle
    * Signed 16bit Integer (Can NULL)
    * Vehicle ID according to [Tockdom.com](https://wiki.tockdom.com/wiki/List_of_Identifiers#Vehicles)
* controller
    * Signed 16bit Integer (Can NULL)
    * Controller ID, UNSAFE, there could be values different than the ones listed below.
        * Refer to this JSON
        ```json
        {
            "0": "Wii Wheel",
            "1": "Nunchuck + Wiimote",
            "2": "Classic Controller",
            "3": "Gamecube Controller",
            "25": "Unknown. Presumably USB GCN?",
        }
        ``` 
* drift
    * bool (Can NULL)
    * Holds whether the run uses automatic or manual drift
        * true = automatic
        * false = manual
* lap1
    * Signed 32bit Integer (Can NULL)
    * Stores in ms the length of lap 1
* lap2
    * Signed 32bit Integer (Can NULL)
    * Stores in ms the length of lap 2
* lap3
    * Signed 32bit Integer (Can NULL)
    * Stores in ms the length of lap 3
* date
    * String (Can NULL)
    * Date of the run stored in "yyyy-mm-dd" format.

## MKW Raw
MKW Raw hosts every time in the database unfiltered. This is meant for last ditch efforts as the file is quite heavy, it's not reccomended.

## MKW Sorted
MKW Sorted hosts every time sorted by something.

### MKW By Track
Hosts every time sorted by track and category. Proper usage is ./mkw/by_track/:track/:category/data.json

### MKW By Player
Hosts every time sorted by player_id. Proper usage is ./mkw/by_player/:player_id/data.json
