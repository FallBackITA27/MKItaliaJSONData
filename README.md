# MKItaliaJSONData
This is a backup of data in JSON format, so that it's accessible for anyone even when the site is down. Might not always be up to date.

# Documentation
* [MKW Documentation](#mkw)
    * [Raw Data](#mkw-raw)
    * [Sorted Data](#mkw-sorted)
        * [By Track](#mkw-by-track)
        * [By Player](#mkw-by-player)

## MKW
Here's the data:
* player_id
    * Signed 32bit Integer
    * Holds the user id. It's One-based, there's no id 0.
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
        * 0 = No Glitch No Shortcut (Normal)
        * 1 = Shortcut
        * 2 = Glitch
* proof_status
    * Signed 16bit Integer
    * Stores the proof's status.
        * 0 = No Proof
        * 1 = To Be Announced
        * 2 = Photo
        * 3 = Video
        * 4 = Revolution Kart Ghost Data (RKG File)
        * 5 = Chadsoft Ghost
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
    * String (Can NULL)
    * Mii data used for the run.
        * This is used for rendering miis. You can render these by using https://studio.mii.nintendo.com/miis/image.png?data=:mii_data=normal&width=512&bgColor=FFFFFF00&clothesColor=default&cameraXRotate=0&cameraYRotate=335&cameraZRotate=0&characterXRotate=0&characterYRotate=0&characterZRotate=0&lightDirectionMode=none&instanceCount=1&instanceRotationMode=model
        * Example:
        
        ![Alt text](https://studio.mii.nintendo.com/miis/image.png?data=000f165d65747e849da0abafb5b7bab4bdbec4cbd3dae6ed040d141b1a2146404b52574a504a4961737b828c93988f&type=face&expression=normal&width=128&bgColor=FFFFFF00&clothesColor=default&cameraXRotate=0&cameraYRotate=335&cameraZRotate=0&characterXRotate=0&characterYRotate=0&characterZRotate=0&lightDirectionMode=none&instanceCount=1&instanceRotationMode=model)
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
        * 0 = Wii Wheel
        * 1 = Nunchuck + Wiimote
        * 2 = Classic Controller
        * 3 = Gamecube Controller
        * 25 = Unknown. Presumably USB GCN?
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
MKW Raw hosts every time in the database unfiltered.

## MKW Sorted
MKW Sorted hosts every time sorted by something.

### MKW By Track
Hosts every time sorted by track and category. Proper usage is ./mkw/by_track/:track/:category/data.json

### MKW By Player
Hosts every time sorted by player_id. Proper usage is ./mkw/by_player/:player_id/data.json