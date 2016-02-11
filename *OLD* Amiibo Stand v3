#include <WaveHC.h>
#include <WaveUtil.h>
#include <Wire.h>
#include <Adafruit_NFCShield_I2C.h>
//#include <MemoryFree.h>

//Loading Strings into PROGMEM to save RAM
#include <avr/pgmspace.h>
//Character Intro File Names
prog_char string_0[] PROGMEM = "cfalc.wav";
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
prog_char string_19[] PROGMEM = "tlink.wav";
prog_char string_20[] PROGMEM = "dede.wav";
prog_char string_21[] PROGMEM = "lucario.wav";
prog_char string_22[] PROGMEM = "bowser.wav";
prog_char string_23[] PROGMEM = "mega.wav";
prog_char string_24[] PROGMEM = "sonic.wav";
prog_char string_25[] PROGMEM = "rosa.wav";
prog_char string_26[] PROGMEM = "mknight.wav";
prog_char string_27[] PROGMEM = "shulk.wav";
prog_char string_28[] PROGMEM = "sheik.wav";
prog_char string_29[] PROGMEM = "ike.wav";
  //Wave 4
prog_char string_60[] PROGMEM = "robin.wav";
prog_char string_61[] PROGMEM = "lucina.wav";
prog_char string_62[] PROGMEM = "char.wav";
prog_char string_63[] PROGMEM = "wario.wav";
prog_char string_64[] PROGMEM = "pacman.wav";
prog_char string_65[] PROGMEM = "ness.wav";
//Songs
prog_char string_30[] PROGMEM = "cfalc_s.wav";
prog_char string_31[] PROGMEM = "samus_s.wav";
prog_char string_32[] PROGMEM = "lmac_s.wav";
prog_char string_33[] PROGMEM = "fox_s.wav";
prog_char string_34[] PROGMEM = "wft_s.wav";
prog_char string_35[] PROGMEM = "vil_s.wav";
prog_char string_36[] PROGMEM = "marth_s.wav";
prog_char string_37[] PROGMEM = "yoshi_s.wav";
prog_char string_38[] PROGMEM = "pit_s.wav";
prog_char string_39[] PROGMEM = "kirby_s.wav";
prog_char string_40[] PROGMEM = "pika_s.wav";
prog_char string_41[] PROGMEM = "link_s.wav";
prog_char string_42[] PROGMEM = "luigi_s.wav";
prog_char string_43[] PROGMEM = "luigi2_s.wav";
prog_char string_44[] PROGMEM = "diddy_s.wav";
prog_char string_45[] PROGMEM = "dk_s.wav";
prog_char string_46[] PROGMEM = "peach_s.wav";
prog_char string_47[] PROGMEM = "zelda_s.wav";
prog_char string_48[] PROGMEM = "mario_s.wav";
prog_char string_49[] PROGMEM = "tlink_s.wav";
prog_char string_50[] PROGMEM = "dede_s.wav";
prog_char string_51[] PROGMEM = "luca_s.wav";
prog_char string_52[] PROGMEM = "bowser_s.wav";
prog_char string_53[] PROGMEM = "mega_s.wav";
prog_char string_54[] PROGMEM = "sonic_s.wav";
prog_char string_55[] PROGMEM = "rosa_s.wav";
prog_char string_56[] PROGMEM = "mknight_s.wav";
prog_char string_57[] PROGMEM = "shulk_s.wav";
prog_char string_58[] PROGMEM = "sheik_s.wav";
prog_char string_59[] PROGMEM = "ike_s.wav";
  //Wave 4
prog_char string_66[] PROGMEM = "robin_s.wav";
prog_char string_67[] PROGMEM = "lucina_s.wav";
prog_char string_68[] PROGMEM = "char_s.wav";
prog_char string_69[] PROGMEM = "wario_s.wav";
prog_char string_70[] PROGMEM = "pacman_s.wav";
prog_char string_71[] PROGMEM = "ness_s.wav";

// Then set up a table to refer to your strings.

PROGMEM const char *string_table[] = 	   
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
  string_18,
  string_19,  
  string_20,  
  string_21,  
  string_22,  
  string_23,  
  string_24,  
  string_25,  
  string_26,  
  string_27,  
  string_28,  
  string_29,  
  string_30,
  string_31,
  string_32,
  string_33,
  string_34,
  string_35,
  string_36,
  string_37,
  string_38,
  string_39,
  string_40,
  string_41,
  string_42,
  string_43,
  string_44,
  string_45,
  string_46,
  string_47,
  string_48,
  string_49,
  string_50,
  string_51,
  string_52,
  string_53,
  string_54,
  string_55,
  string_56,
  string_57,
  string_58,
  string_59,
  string_60,
  string_61,
  string_62,
  string_63,
  string_64,
  string_65,
  string_66,
  string_67,
  string_68,
  string_69,
  string_70,
  string_71,  };

char buffer[71];

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
uint32_t versiondata;

//My Added Variables
uint32_t lastcard = 0;
uint32_t currentcard = 1;
uint32_t CID = 0;
boolean songplaying = false;

//Loop()
uint32_t cardidentifier = 0;
uint8_t success;
uint8_t uid[] = { 0, 0, 0, 0, 0, 0, 0 }; // Buffer to store the returned UID
uint8_t uidLength; // Length of the UID (4 or 7 bytes depending on ISO14443A card type)
 
//////////////////////////////////// SETUP

void setup() {
  // set up Serial library at 9600 bps
  Serial.begin(115200);
    
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
  
  PgmPrintln("Files found:");
  root.ls();
  
  // find Adafruit RFID/NFC shield
  nfc.begin();

  versiondata = nfc.getFirmwareVersion();
  if (! versiondata) {
    Serial.print(F("Didn't find PN53x board"));
    while (1); // halt
  }
  // Got ok data, print it out!
  Serial.print(F("Found chip PN5")); Serial.println((versiondata>>24) & 0xFF, HEX);
  Serial.print(F("Firmware ver. ")); Serial.print((versiondata>>16) & 0xFF, DEC);
  Serial.print('.'); Serial.println((versiondata>>8) & 0xFF, DEC);
  
  // configure board to read RFID tags
  nfc.SAMConfig();
  
  //enable timeout waiting for cards
  nfc.setPassiveActivationRetries(50);

}

/////////////////////////////////// LOOP

unsigned digit = 0;

void loop() 
{
  
  //Memory Checker
  
  //Serial.print(F("Memory Available = "));
  //Serial.println(freeMemory());
  
  
  // wait for RFID card to show up!
  Serial.println(F("Waiting for an Amiibo ..."));

    
  // Wait for an ISO14443A type cards (Mifare, etc.). When one is found
  // 'uid' will be populated with the UID, and uidLength will indicate
  // if the uid is 4 bytes (Mifare Classic) or 7 bytes (Mifare Ultralight)
  success = nfc.readPassiveTargetID(PN532_MIFARE_ISO14443A, uid, &uidLength);

  cardidentifier = 0;
  CID = 999; 
  if (success) 
  {
    // Found a card!

    Serial.print(F("Amiibo detected #"));
    // turn the four byte UID of a mifare classic into a single variable #
    cardidentifier = uid[3];
    cardidentifier <<= 8; cardidentifier |= uid[2];
    cardidentifier <<= 8; cardidentifier |= uid[1];
    cardidentifier <<= 8; cardidentifier |= uid[0];
    Serial.println(cardidentifier);
    
    //Check the previous card
    
    (lastcard = currentcard);
    (currentcard = cardidentifier);
    
    Serial.print(F("Last Amiibo:    #"));
    Serial.println(lastcard);
    Serial.print(F("Current Card:"));
    Serial.println(currentcard);
    
    // Check Character ID
    
      // Try to read the Character info page (#21)
      uint8_t charID[32];
      success = nfc.mifareultralight_ReadPage (21, charID);
      
    if (success)
    {
        // turn page 21 into a character ID
      CID = charID[6];
      CID <<= 8; CID |= charID[6];
      CID <<= 8; CID |= charID[5];
      CID <<= 8; CID |= charID[4];
      CID <<= 8; CID |= charID[3];
      CID <<= 8; CID |= charID[2];
      CID <<= 8; CID |= charID[1];
      CID <<= 8; CID |= charID[0];
      Serial.println("Character Number: ");
      Serial.println(CID);
    
    
      if (currentcard == lastcard) 
      {
      /*
        If there is no song playing, play a song.
      */
        if (songplaying == false) 
        {
          //Captain Falcon Song
          if (CID == 6)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[30])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Samus Song
          if (CID == 49157)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[31])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Little Mac Song
          if (CID == 49158)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[32])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Fox Song
          if (CID == 32773)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[33])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
         //Wii Fit Song 
          if (CID == 7)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[34])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Villager Song        
          if (CID == 32769)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[35])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Marth Song
          if (CID == 33)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[36])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Yoshi Song
          if (CID == 768)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[37])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Pit Song
          if (CID == 16391)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[38])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Kirby Song
          if (CID == 31)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[39])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Pikachu Song
          if (CID == 6425)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[40])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Link Song
          if (CID == 1)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[41])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Luigi Song
          if (CID == 256)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[42])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Diddy Song
          if (CID == 2304)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[44])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //DK Song
          if (CID == 2048)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[45])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Peach Song
          if (CID == 512)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[46])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Zelda Song
          if (CID == 257)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[47])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Mario Song
          if (CID == 0)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[48])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Toonlink Song
          if (CID == 65537)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[49])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Dedede Song
          if (CID == 543)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[50])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Lucario Song
          if (CID == 49178)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[51])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Bowser Song
          if (CID == 1280)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[52])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Mega Man Song
          if (CID == 32820)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[53])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Sonic Song
          if (CID == 50)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[54])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Rosalina Song
          if (CID == 66560)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[55])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //MetaKnight Song
          if (cardidentifier == 287)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[56])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Shulk Song
          if (CID == 16418)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[57])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Sheik Song
          if (CID == 65793)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[58])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Ike Song
          if (CID == 289)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[59])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
        }
        
        if(!wave.isplaying) 
        {
          songplaying = false;
        }  
      }
      /*
        There is no song playing, play the intro sequence!
      */
      else 
      {
        //Captain Falcon
        if (CID == 6) 
        {
          strcpy_P(buffer, (char*)pgm_read_word(&(string_table[0])));
          playcomplete(buffer);
        }
        //Samus
        if (CID == 49157) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[1])));
          playcomplete(buffer);
        }
        //Little Mac
        if (CID == 49158) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[2])));
          playcomplete(buffer);
        }
        //Fox
        if (CID == 32773) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[3])));
          playcomplete(buffer);
        }
        //Wii Fit
        if (CID == 7) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[4])));
          playcomplete(buffer);
        }
        //Villager
        if (CID == 32769) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[5])));
          playcomplete(buffer);
        }
        //Marth
        if (CID == 33) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[6])));
          playcomplete(buffer);
        }
        //Yoshi
        if (CID == 768) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[7])));
          playcomplete(buffer);
        }
        //Pit
        if (CID == 16391) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[8])));
          playcomplete(buffer);
        }
        //Kirby
        if (CID == 31) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[9])));
          playcomplete(buffer);
        }
        //Pikachu
        if (CID == 6425) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[10])));
          playcomplete(buffer);
        }
        //Link
        if (CID == 1) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[11])));
          playcomplete(buffer);
        }
        //Luigi
        if (CID == 256) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[12])));
          playcomplete(buffer);
        }
        //Diddy Kong
        if (CID == 2304) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[14])));
          playcomplete(buffer);
        }
        //DK
        if (CID == 2048) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[15])));
          playcomplete(buffer);
        }
        //Peach
        if (CID == 512) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[16])));
          playcomplete(buffer);
        }
        //Zelda
        if (CID == 257) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[17])));
          playcomplete(buffer);
        }
        //Mario
        if (CID == 0) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[18])));
          playcomplete(buffer);
        }
        //Toon Link
        if (CID == 65537) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[19])));
          playcomplete(buffer);
        }
        //Dedede
        if (CID == 543) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[20])));
          playcomplete(buffer);
        }
        //Lucario
        if (CID == 49178) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[21])));
          playcomplete(buffer);
        }
        //Bowser
        if (CID == 1280) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[22])));
          playcomplete(buffer);
        }
        //Mega Man
        if (CID == 32820) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[23])));
          playcomplete(buffer);
        }
        //Sonic
        if (CID == 50) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[24])));
          playcomplete(buffer);
        }
        //Rosalina
        if (CID == 66560) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[25])));
          playcomplete(buffer);
        }
        //Meta Knight
        if (CID == 287) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[26])));
          playcomplete(buffer);
        }
        //Shulk
        if (CID == 16418) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[27])));
          playcomplete(buffer);
        }
        //Sheik
        if (CID == 65793) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[28])));
          playcomplete(buffer);
        }
        //Ike
        if (CID == 289) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[29])));
          playcomplete(buffer);
        }
      }
    }
    else 
    {
      //if (currentcard == lastcard) 
      //{
       // Serial.println("CID else");
        wave.stop();
      //}  
      lastcard = 123456;
      currentcard = 654321;
      songplaying = false;
    }
  } 

   //If the Amiibo is gone, stop the song.
  else 
    {
      //if (currentcard == lastcard) 
      //{
        //Serial.println("UID else");
        wave.stop();
      //}  
      lastcard = 321123;
      currentcard = 123321;
      songplaying = false;
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
