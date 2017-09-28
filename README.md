# OSD Library for Arduino
This is a Library for OSD,the function is the superposition of characters
## Table of Contents

* [Summary](#summary)
* [Methods](#methods)
* [Compatibility](#compatibility)
* [History](#history)
* [Tool\(Custom Chinese characters\)](#tool\(custom chinese characters\))
* [Credits](#credits)

<snippet>
<content>

## Summary
This is a Library for OSD,the function is the superposition of characters.And You can display certain characters on screen.

## Methods

```C++

#include <DFRobot_OSD.h>
/*
 * @brief Init OSD
 *
 * @param CS Selection pin
 */
void init(int CS);

/*
 * @brief Clear screen
 */
void clear(void);

/*
 * @brief display char of AT7456E's first page EEPROM library
 *
 * @param row Horizontal coordinate, range(0,15)
 * @param col Vertical coordinate, range(0,29)
 * @param c Address of char
 */
void displayChar(unsigned char row, unsigned char col, unsigned char c);

/*
 * @brief display string,the first page EEPROM font of AT7456E
 *
 * @param row Horizontal coordinate, range(0,15)
 * @param col Vertical coordinate, range(0,29)
 * @param s String
 */
void displayString(unsigned char row, unsigned char col, unsigned char *s); 

/*
 * @brief display char of AT7456E's first and second page EEPROM library
 *
 * @param row Horizontal coordinate, range(0,15)
 * @param col Vertical coordinate, range(0,29)
 * @param value Address of char
 */
void AT7456EChar(unsigned char row, unsigned char col, short value);

/*
 * @brief display string,all of character in EEPROM font of AT7456E
 *
 * @param row Horizontal coordinate, range(0,15)
 * @param col Vertical coordinate, range(0,29)
 * @param s String
 */
void AT7456EString(unsigned char row, unsigned char col, unsigned char *s);

/*
 * @brief Write the custom character to the OSD, replacing the original character
 *
 * @param addr Address of the stored character
 * @param dt Array generated through the tool
 */
void changeChar(unsigned short addr,int dt[]);

```

## Compatibility

MCU                | Work Well | Work Wrong | Untested  | Remarks
------------------ | :----------: | :----------: | :---------: | -----
firebeetle board328p |      √       |             |            | 
firebeetle esp32 |      √       |             |            | 
firebeetle esp8266 |      √       |             |            | 
Leonardo |      √       |             |            | 

## History

- data 2017-9-27
- version V1.0


## Tool(Custom Chinese characters)
* congfig <br>
![image](https://github.com/DFRobot/DFRobot_OSD/blob/master/image/config.png)

* output <br>
![image](https://github.com/DFRobot/DFRobot_OSD/blob/master/image/putout.png)

## Credits

- author [Luyuhao  <yuhao.lu@dfrobot.com>]
