# ADAM ASMACA V4.5.0 README FILE
## Overview

This is a README file for the Hangman game.

## Installation

Run the [setup.py](setup.py) file in the directory to install the [PyYaml](https://pypi.org/project/PyYAML/) library.

```bash
pip install pyyaml
```
## How to Play
After installation, simply run the game.py file to start the game.

## Features
Login/Signup for each user
Users can log in and their accounts will be saved.

## Admin Mode:
    Access and modify game files.
    Add a new word to a category.
    Add a new category.
    Play the game in admin mode (not saved).
    View game run settings (basic values displayed at once).
## CONFIG File
A configuration file that allows you to edit all game settings.

Example Config:
```yaml
admin_kullanici_adi: admin
admin_sifresi: cokgizlisifre

# Are games saved? Any value except True is considered False.
Oyunlar_Kaydedilsinmi: True

# Starting coin for a player starting a game. THIS VALUE SHOULD NEVER BE 0 OR FALSE. SIMILARLY, DO NOT USE 0 OR FALSE FOR ANY OTHER VALUES BELOW. SIMPLY USE A NON-TRUE VALUE.
Baslama_coini: 1

# Coin-giving calculations after a game, which depend on the length of the word and the difficulty level of the game.
COIN_Kolay_Carpani: 2
COIN_Normal_Carpani: 5
COIN_Zor_Carpani: 10

# Costs of getting a letter.
COIN_Kolay_Harf_Alma_Bedeli: 8
COIN_Normal_Harf_Alma_Bedeli: 20
COIN_Zor_Harf_Alma_Bedeli: 40

# Security Protocol:
# 0) No security.
# 1) Password of at least 8 characters.
# 2) Password of at least 8 characters with at least one number.
# 3) Password of at least 8 characters with at least one number and uppercase and lowercase letters.
# 4) Password of at least 8 characters with at least one number, uppercase and lowercase letters, and special characters.
guvenlik_protokolu: 2

# Do not modify.
config_version: 4.5.0_PB_RLS_BqUtsZ985
```
Except for the number of lives, all values can be edited in the config.yaml file.
## Game Mode Selection
-Easy Mode:

    +12 lives.
    +Categories is visible
    +Remaining lives * 5 point multiplier.
    +Cost of a letter is set in the config.
-Medium Mode:

    6 lives.
    Categories is visible
    Remaining lives * 10 point multiplier.
    Cost of a letter is set in the config.
-Hard Mode:

    4 lives.
    Categories isn't visible
    Remaining lives * 30 point multiplier.
    Cost of a letter is set in the config.


## Realistic Hangman Game:
    The hangman is displayed on the screen according to your remaining lives.
    The length of the word is displayed with underscores, for example, the word "apple" would be displayed as "_ _ _ _ _".
    Your score is calculated according to your remaining lives.
    Your wins and losses are recorded.
## Game Record Format:
Main Lang Is TR So;
```yaml
    Oyun -> <tarih>-<saat>:
        Oyun zorluk modu: <>
        Kazanilan Oyun Sayisi: <>
        Kaybedilen Oyun Sayisi: <>
        Kazanilan Puan: <>
        Oyun Suresi: <saat-dakika-saniye>
```

## File Locations:
    Accounts --» data/main/accounts.txt (format = <username>?<password>)
    Categories --» data/main/categories/ (all categories are available in the folder, all.txt file contains all category names)
    Save Files --» data/player.saves/<username>.txt
## Coin System:

    Each match earns coins based on the difficulty coefficient which is calculated by multiplying the length of the word with the difficulty level. These coins can be used to reveal a hidden letter with the !harfal command.
## Statistics:
    Players can view their stats in the login section.

    Example:
```yaml
Statistics for Player XoX:
Total games won: 1
Total games lost: 0
Total time spent in games: 1:20
Total score: 105
Current coins: 950
```
## Colorful Game Experience:
    The game is fully colored and decorated with ASCII ART.

## License

[MIT](https://choosealicense.com/licenses/mit/)
