#include <WaveHC.h>
#include <WaveUtil.h>
#include <Wire.h>
#include <Adafruit_NFCShield_I2C.h>
#include <MemoryFree.h>

//PROGMEM Test
#include <avr/pgmspace.h>
prog_char string_0[] PROGMEM = "cfalc.wav";   // "String 0" etc are strings to store - change to suit.
prog_char string_1[] PROGMEM = "samus.wav";
prog_char string_2[] PROGMEM = "lmac.wav";
prog_char string_3[] PROGMEM = "fox.wav";
prog_char string_4[] PROGMEM = "wft.wav";
prog_char string_5[] PROGMEM = "villager.wav";
prog_char string_6[] PROGMEM = "marth.wav";
prog_char string_7[] PROGMEM = "yoshi.wav";
prog_char string_8[] PROGMEM = "pit.wav";
prog_char string_9[] PROGMEM = "kirby.wav";
prog_char string_10[] PROGMEM = "pikachu.wav";
prog_char string_11[] PROGMEM = "link.wav";
prog_char string_12[] PROGMEM = "luigi.wav";
prog_char string_13[] PROGMEM = "luigi2.wav";
prog_char string_14[] PROGMEM = "diddy.wav";
prog_char string_15[] PROGMEM = "dk.wav";
prog_char string_16[] PROGMEM = "peach.wav";
prog_char string_17[] PROGMEM = "zelda.wav";
prog_char string_18[] PROGMEM = "mario.wav";

// Then set up a table to refer to your strings.

PROGMEM const char *string_table[] = 	   // change "string_table" name to suit
{   
  string_0,
  string_1,
  string_2,
  string_3,
  string_4,
  string_5,
  string_6,
  string_7,
  string_8,
  string_9,
  string_10,
  string_11,
  string_12,
  string_13,
  string_14,
  string_15,
  string_16,
  string_17,
  string_18,  };

char buffer[30];

#define IRQ 6 // this trace must be cut and rewired!
#define RESET 8

Adafruit_NFCShield_I2C nfc(IRQ, RESET);

SdReader card; // This object holds the information for the card
FatVolume vol; // This holds the information for the partition on the card
FatReader root; // This holds the information for the volumes root directory
FatReader file; // This object represent the WAV file for a pi digit or period
WaveHC wave; // This is the only wave (audio) object, since we will only play one at a time
/*
* Define macro to put error messages in flash memory
*/
#define error(msg) error_P(PSTR(msg))

//Setup()
//uint32_t versiondata;

//My Added Variables
uint32_t lastcard = 0;
uint32_t currentcard;

//Loop()
uint32_t cardidentifier = 0;
uint8_t success;
uint8_t uid[] = { 0, 0, 0, 0, 0, 0, 0 }; // Buffer to store the returned UID
uint8_t uidLength; // Length of the UID (4 or 7 bytes depending on ISO14443A card type)
 
//////////////////////////////////// SETUP

void setup() {
  // set up Serial library at 9600 bps
  Serial.begin(9600);
    
  PgmPrintln("Amiibo Scanner");
  
  if (!card.init()) {
    error("Card init. failed!");
  }
  if (!vol.init(card)) {
    error("No partition!");
  }
  if (!root.openRoot(vol)) {
    error("Couldn't open dir");
  }
  /*
  PgmPrintln("Files found:");
  root.ls();
  */
  // find Adafruit RFID/NFC shield
  nfc.begin();
/*
  versiondata = nfc.getFirmwareVersion();
  if (! versiondata) {
    Serial.print(F("Didn't find PN53x board"));
    while (1); // halt
  }
  // Got ok data, print it out!
  Serial.print(F("Found chip PN5")); Serial.println((versiondata>>24) & 0xFF, HEX);
  Serial.print(F("Firmware ver. ")); Serial.print((versiondata>>16) & 0xFF, DEC);
  Serial.print('.'); Serial.println((versiondata>>8) & 0xFF, DEC);
  */
  // configure board to read RFID tags
  nfc.SAMConfig();
  
  //enable timeout waiting for cards
  nfc.setPassiveActivationRetries(500);

}

/////////////////////////////////// LOOP

unsigned digit = 0;

void loop() {
  
  //Memory Checker
  
  Serial.print(F("Memory Available = "));
  Serial.println(freeMemory());
  
  
  // wait for RFID card to show up!
  Serial.println(F("Waiting for an ISO14443A Card ..."));

    
  // Wait for an ISO14443A type cards (Mifare, etc.). When one is found
  // 'uid' will be populated with the UID, and uidLength will indicate
  // if the uid is 4 bytes (Mifare Classic) or 7 bytes (Mifare Ultralight)
  success = nfc.readPassiveTargetID(PN532_MIFARE_ISO14443A, uid, &uidLength);

  cardidentifier = 0;
   
  if (success) {
    // Found a card!

    Serial.print(F("Card detected #"));
    // turn the four byte UID of a mifare classic into a single variable #
    cardidentifier = uid[3];
    cardidentifier <<= 8; cardidentifier |= uid[2];
    cardidentifier <<= 8; cardidentifier |= uid[1];
    cardidentifier <<= 8; cardidentifier |= uid[0];
    Serial.println(cardidentifier);
    
    //Check the previous card
    
    (lastcard = currentcard);
    (currentcard = cardidentifier);
    
    Serial.print(F("Last Card:"));
    Serial.println(lastcard);
    Serial.print(F("Current Card:"));
    Serial.println(currentcard);
    
  // repeat this for loop as many times as you have RFID cards
    if (currentcard == lastcard) {
    }
    
    else {
      
      if (cardidentifier == 3266796292) 
      {
        strcpy_P(buffer, (char*)pgm_read_word(&(string_table[0])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 1519730948) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[1])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 3125957124) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[2])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 2456861188) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[3])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 3270290948) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[4])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 3398987780) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[5])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 2186368004) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[6])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 2057060100) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[7])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 581738756) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[8])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 1648956676) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[9])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 1653835268) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[10])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 719015684) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[11])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 3264737284) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[12])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 3259030020) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[13])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 851602436) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[14])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 3673369860) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[15])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 2458258948) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[16])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 2588707844) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[17])));
        playcomplete(buffer);
      }
      
      if (cardidentifier == 3401629188) 
      {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[18])));
        playcomplete(buffer);
      }
    }
  }
  else {
    lastcard = 0;
    currentcard = 1;
  } 
}

/////////////////////////////////// HELPERS

/*
* print error message and halt
*/
void error_P(const char *str) {
  PgmPrint("Error: ");
  SerialPrint_P(str);
  sdErrorCheck();
  while(1);
}
/*
* print error message and halt if SD I/O error
*/
void sdErrorCheck(void) {
  if (!card.errorCode()) return;
  PgmPrint("\r\nSD I/O error: ");
  Serial.print(card.errorCode(), HEX);
  PgmPrint(", ");
  Serial.println(card.errorData(), HEX);
  while(1);
}
/*
* Play a file and wait for it to complete
*/
void playcomplete(char *name) {
  playfile(name);
  while (wave.isplaying);
  
  // see if an error occurred while playing
  sdErrorCheck();
}
/*
* Open and start playing a WAV file
*/
void playfile(char *name) {
  if (wave.isplaying) {// already playing something, so stop it!
    wave.stop(); // stop it
  }
  if (!file.open(root, name)) {
    PgmPrint("Couldn't open file ");
    Serial.print(name);
    return;
  }
  if (!wave.create(file)) {
    PgmPrintln("Not a valid WAV");
    return;
  }
  // ok time to play!
  wave.play();
}
