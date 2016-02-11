#include <WaveHC.h>
#include <WaveUtil.h>
#include <Wire.h>
#include <Adafruit_NFCShield_I2C.h>
//#include <MemoryFree.h>

//Loading Strings into PROGMEM to save RAM
#include <avr/pgmspace.h>
//Character Intro File Names
const char string_0[] PROGMEM = "cfalc.wav";
const char string_1[] PROGMEM = "samus.wav";
const char string_2[] PROGMEM = "lmac.wav";
const char string_3[] PROGMEM = "fox.wav";
const char string_4[] PROGMEM = "wft.wav";
const char string_5[] PROGMEM = "villager.wav";
const char string_6[] PROGMEM = "marth.wav";
const char string_7[] PROGMEM = "yoshi.wav";
const char string_8[] PROGMEM = "pit.wav";
const char string_9[] PROGMEM = "kirby.wav";
const char string_10[] PROGMEM = "pikachu.wav";
const char string_11[] PROGMEM = "link.wav";
const char string_12[] PROGMEM = "luigi.wav";
const char string_13[] PROGMEM = "luigi2.wav";
const char string_14[] PROGMEM = "diddy.wav";
const char string_15[] PROGMEM = "dk.wav";
const char string_16[] PROGMEM = "peach.wav";
const char string_17[] PROGMEM = "zelda.wav";
const char string_18[] PROGMEM = "mario.wav";
const char string_19[] PROGMEM = "tlink.wav";
const char string_20[] PROGMEM = "dede.wav";
const char string_21[] PROGMEM = "lucario.wav";
const char string_22[] PROGMEM = "bowser.wav";
const char string_23[] PROGMEM = "mega.wav";
const char string_24[] PROGMEM = "sonic.wav";
const char string_25[] PROGMEM = "rosa.wav";
const char string_26[] PROGMEM = "mk.wav";
const char string_27[] PROGMEM = "shulk.wav";
const char string_28[] PROGMEM = "sheik.wav";
const char string_29[] PROGMEM = "ike.wav";
  //Wave 4 - Intros
const char string_60[] PROGMEM = "robin.wav";
const char string_61[] PROGMEM = "lucina.wav";
const char string_62[] PROGMEM = "char.wav";
const char string_63[] PROGMEM = "wario.wav";
const char string_64[] PROGMEM = "pacman.wav";
const char string_65[] PROGMEM = "ness.wav";
const char string_66[] PROGMEM = "ganon.wav";
const char string_67[] PROGMEM = "gren.wav";
const char string_68[] PROGMEM = "jiggly.wav";
  //Wave 5+ - Intros
const char string_78[] PROGMEM = "dpit.wav";
const char string_80[] PROGMEM = "palu.wav";
const char string_81[] PROGMEM = "zss.wav";
const char string_82[] PROGMEM = "dmario.wav";
const char string_83[] PROGMEM = "bowjr.wav";
const char string_84[] PROGMEM = "olimar.wav";
const char string_85[] PROGMEM = "mrgw.wav";
const char string_86[] PROGMEM = "rob.wav";
const char string_87[] PROGMEM = "duck.wav";
const char string_88[] PROGMEM = "miib.wav";
const char string_89[] PROGMEM = "miis.wav";
const char string_90[] PROGMEM = "miig.wav";
const char string_91[] PROGMEM = "mewtwo.wav";
const char string_92[] PROGMEM = "falco.wav";
const char string_93[] PROGMEM = "lucas.wav";
const char string_94[] PROGMEM = "shovelk.wav";
const char string_95[] PROGMEM = "roy.wav";
const char string_96[] PROGMEM = "ryu.wav";
const char string_97[] PROGMEM = "cloud.wav";
const char string_98[] PROGMEM = "bayo.wav";
const char string_99[] PROGMEM = "corrin.wav";
  //Non-Smash Intros
const char string_120[] PROGMEM = "inkg.wav";
const char string_121[] PROGMEM = "inkb.wav";
const char string_122[] PROGMEM = "squid.wav";
const char string_123[] PROGMEM = "chibi.wav";
const char string_124[] PROGMEM = "yarn.wav";
const char string_125[] PROGMEM = "isab.wav";
const char string_126[] PROGMEM = "nook.wav";
const char string_127[] PROGMEM = "kk.wav";
const char string_128[] PROGMEM = "mabel.wav";
const char string_129[] PROGMEM = "digby.wav";
const char string_130[] PROGMEM = "lott.wav";
const char string_131[] PROGMEM = "cyrus.wav";
const char string_132[] PROGMEM = "reese.wav";
const char string_133[] PROGMEM = "blath.wav";
const char string_134[] PROGMEM = "cele.wav";
const char string_135[] PROGMEM = "reset.wav";
const char string_136[] PROGMEM = "kicks.wav";
const char string_137[] PROGMEM = "timtom.wav";
const char string_138[] PROGMEM = "kappn.wav";
const char string_139[] PROGMEM = "rover.wav";
const char string_140[] PROGMEM = "wlink.wav";

//Songs
const char string_30[] PROGMEM = "cfalc_s.wav";
const char string_31[] PROGMEM = "samus_s.wav";
const char string_32[] PROGMEM = "lmac_s.wav";
const char string_33[] PROGMEM = "fox_s.wav";
const char string_34[] PROGMEM = "wft_s.wav";
const char string_35[] PROGMEM = "vil_s.wav";
const char string_36[] PROGMEM = "marth_s.wav";
const char string_37[] PROGMEM = "yoshi_s.wav";
const char string_38[] PROGMEM = "pit_s.wav";
const char string_39[] PROGMEM = "kirby_s.wav";
const char string_40[] PROGMEM = "pika_s.wav";
const char string_41[] PROGMEM = "link_s.wav";
const char string_42[] PROGMEM = "luigi_s.wav";
const char string_43[] PROGMEM = "luigi2_s.wav";
const char string_44[] PROGMEM = "diddy_s.wav";
const char string_45[] PROGMEM = "dk_s.wav";
const char string_46[] PROGMEM = "peach_s.wav";
const char string_47[] PROGMEM = "zelda_s.wav";
const char string_48[] PROGMEM = "mario_s.wav";
const char string_49[] PROGMEM = "tlink_s.wav";
const char string_50[] PROGMEM = "dede_s.wav";
const char string_51[] PROGMEM = "luca_s.wav";
const char string_52[] PROGMEM = "bowser_s.wav";
const char string_53[] PROGMEM = "mega_s.wav";
const char string_54[] PROGMEM = "sonic_s.wav";
const char string_55[] PROGMEM = "rosa_s.wav";
const char string_56[] PROGMEM = "mk_s.wav";
const char string_57[] PROGMEM = "shulk_s.wav";
const char string_58[] PROGMEM = "sheik_s.wav";
const char string_59[] PROGMEM = "ike_s.wav";
  //Wave 4
const char string_69[] PROGMEM = "robin_s.wav";
const char string_70[] PROGMEM = "lucina_s.wav";
const char string_71[] PROGMEM = "char_s.wav";
const char string_72[] PROGMEM = "wario_s.wav";
const char string_73[] PROGMEM = "pac_s.wav";
const char string_74[] PROGMEM = "ness_s.wav";
const char string_75[] PROGMEM = "ganon_s.wav";
const char string_76[] PROGMEM = "gren_s.wav";
const char string_77[] PROGMEM = "jiggly_s.wav";
  //Wave 5+
const char string_79[] PROGMEM = "dpit_s.wav";
const char string_100[] PROGMEM = "palu_s.wav";
const char string_101[] PROGMEM = "zss_s.wav";
const char string_102[] PROGMEM = "dmaro_s.wav";
const char string_103[] PROGMEM = "bowjr_s.wav";
const char string_104[] PROGMEM = "olimar_s.wav";
const char string_105[] PROGMEM = "mrgw_s.wav";
const char string_106[] PROGMEM = "rob_s.wav";
const char string_107[] PROGMEM = "duck_s.wav";
const char string_108[] PROGMEM = "miib_s.wav";
const char string_109[] PROGMEM = "miis_s.wav";
const char string_110[] PROGMEM = "miig_s.wav";
const char string_111[] PROGMEM = "mewtwo_s.wav";
const char string_112[] PROGMEM = "falco_s.wav";
const char string_113[] PROGMEM = "lucas_s.wav";
const char string_114[] PROGMEM = "shovelk_s.wav";
const char string_115[] PROGMEM = "roy_s.wav";
const char string_116[] PROGMEM = "ryu_s.wav";
const char string_117[] PROGMEM = "cloud_s.wav";
const char string_118[] PROGMEM = "bayo_s.wav";
const char string_119[] PROGMEM = "corrin_s.wav";
  //Non-Smash
const char string_141[] PROGMEM = "inkg_s.wav";
const char string_142[] PROGMEM = "inkb_s.wav";
const char string_143[] PROGMEM = "squid_s.wav";
const char string_144[] PROGMEM = "chibi_s.wav";
const char string_145[] PROGMEM = "yarn_s.wav";
const char string_146[] PROGMEM = "isab_s.wav";
const char string_147[] PROGMEM = "nook_s.wav";
const char string_148[] PROGMEM = "kk_s.wav";
const char string_149[] PROGMEM = "mabel_s.wav";
const char string_150[] PROGMEM = "digby_s.wav";
const char string_151[] PROGMEM = "lott_s.wav";
const char string_152[] PROGMEM = "cyrus_s.wav";
const char string_153[] PROGMEM = "reese_s.wav";
const char string_154[] PROGMEM = "blath_s.wav";
const char string_155[] PROGMEM = "cele_s.wav";
const char string_156[] PROGMEM = "reset_s.wav";
const char string_157[] PROGMEM = "kicks_s.wav";
const char string_158[] PROGMEM = "timtom_s.wav";
const char string_159[] PROGMEM = "kappn_s.wav";
const char string_160[] PROGMEM = "rover_s.wav";
const char string_161[] PROGMEM = "wlink_s.wav";
// Then set up a table to refer to your strings.

const char* const string_table[] PROGMEM = 	   
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
  string_71,
  string_72,
  string_73,
  string_74,
  string_75,
  string_76,
  string_77,
  string_78,
  string_79,
  string_80,
  string_81,
  string_82,
  string_83,
  string_84,
  string_85,
  string_86,
  string_87,
  string_88,
  string_89,
  string_90,
  string_91,
  string_92,
  string_93,
  string_94,
  string_95,
  string_96,
  string_97,
  string_98,
  string_99,
  string_100,
  string_101,
  string_102,
  string_103,
  string_104,
  string_105,
  string_106,
  string_107,
  string_108,
  string_109,
  string_110,
  string_111,
  string_112,
  string_113,
  string_114,
  string_115,
  string_116,
  string_117,
  string_118,
  string_119,
  string_120,
  string_121,
  string_122,
  string_123,
  string_124,
  string_125,
  string_126,
  string_127,
  string_128,
  string_129,
  string_130,
  string_131,
  string_132,
  string_133,
  string_134,
  string_135,
  string_136,
  string_137,
  string_138,
  string_139,
  string_140,
  string_141,
  string_142,
  string_143,
  string_144,
  string_145,
  string_146,
  string_147,
  string_148,
  string_149,
  string_150,
  string_151,
  string_152,
  string_153,
  string_154,
  string_155,
  string_156,
  string_157,
  string_158,
  string_159,
  string_160,
  string_161,
  };

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
  // set up Serial library at 115200 bps
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
          //Robin Song
          if (CID == 801)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[69])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Lucina Song
          if (CID == 545)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[70])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Charizard Song
          if (CID == 1561)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[71])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Wario Song
          if (CID == 1792)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[72])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Pac-Man Song
          if (CID == 16435)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[73])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Ness Song
          if (CID == 32802)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[74])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Gannondorf Song
          if (CID == 66049)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[75])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Greninja Song
          if (CID == 37403)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[76])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Jigglypuff Song
          if (CID == 10009)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[77])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Dark Pit Song
          if (CID == 16647)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[79])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Palutena Song
          if (CID == 16903)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[100])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Zero Suit Song
          if (CID == 114693)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[101])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Dr Mario Song
          if (CID == 65536)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[102])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Bowser Jr Song
          if (CID == 1536)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[103])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Olimar Song
          if (CID == 81926)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[104])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Mr Game & Watch Song
          if (CID == 32775)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[105])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Rob Song
          if (CID == 33031)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[106])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Duck Hunt Song
          if (CID == 33287)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[107])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Mii Brawler Song
          if (CID == 49159)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[108])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Mii Swordfighter Song
          if (CID == 114695)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[109])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Mii Gunner Song
          if (CID == 180231)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[110])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Mewtwo Song
          if (CID == 38425)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[111])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Falco Song
          if (CID == 33029)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[112])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Lucas Song
          if (CID == 33058)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[113])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Shovel Knight Song
          if (CID == 49205)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[114])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Roy Song
          if (CID == 1234)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[115])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Ryu Song
          if (CID == 1234)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[116])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Cloud Song
          if (CID == 1234)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[117])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Corrin Song
          if (CID == 1234)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[118])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Bayonetta Song
          if (CID == 1234)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[119])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
        //Non-Smash
          //Inkling Girl Song
          if (CID == 65544)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[141])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Inkling Boy Song
          if (CID == 131080)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[142])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Squid Song
          if (CID == 196616)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[143])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Chibi Robo Song
          if (CID == 49186)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[144])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Yarn Yoshi Song
          if (CID == 33620736)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[145])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Isabelle Song
          if (CID == 98561)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[146])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Tom Nook Song
          if (CID == 33537)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[147])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //KK Song
          if (CID == 33281)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[148])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Mabel Song
          if (CID == 34817)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[149])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Digby Song
          if (CID == 35841)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[150])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Lottie Song
          if (CID == 49409)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[151])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Cyrus Song
          if (CID == 35585)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[152])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Reese Song
          if (CID == 35329)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[153])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Blathers Song
          if (CID == 37377)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[154])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Celeste Song
          if (CID == 37633)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[155])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Resetti Song
          if (CID == 36353)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[156])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Kicks Song
          if (CID == 37889)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[157])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Timmy and Tommy Song
          if (CID == 1234)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[158])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Kapp'n Song
          if (CID == 1234)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[159])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Rover Song
          if (CID == 1234)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[160])));
            playfile(buffer);
            if (wave.isplaying) {
              songplaying = true;
            }
          }
          //Wolf Link Song
          if (CID == 1234)      
          {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[161])));
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
        //Robin
        if (CID == 801) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[60])));
          playcomplete(buffer);
        }
        //Lucina
        if (CID == 545) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[61])));
          playcomplete(buffer);
        }
        //Charizard
        if (CID == 1561) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[62])));
          playcomplete(buffer);
        }
        //Wario
        if (CID == 1792) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[63])));
          playcomplete(buffer);
        }
        //Pac-Man
        if (CID == 16435) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[64])));
          playcomplete(buffer);
        }
        //Ness
        if (CID == 32802) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[65])));
          playcomplete(buffer);
        }
        //Gannondorf
        if (CID == 66049) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[66])));
          playcomplete(buffer);
        }
        //Greninja
        if (CID == 37403) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[67])));
          playcomplete(buffer);
        }
        //Jigglypuff
        if (CID == 10009) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[68])));
          playcomplete(buffer);
        }
        //Dark Pit
        if (CID == 16647) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[78])));
          playcomplete(buffer);
        }
        //Palutena
        if (CID == 16903) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[80])));
          playcomplete(buffer);
        }
        //Zero suit
        if (CID == 114693) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[81])));
          playcomplete(buffer);
        }
        //Dr Mario
        if (CID == 65536) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[82])));
          playcomplete(buffer);
        }
        //Bowser Jr
        if (CID == 1536) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[83])));
          playcomplete(buffer);
        }
        //Olimar
        if (CID == 81926) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[84])));
          playcomplete(buffer);
        }
        //Mr Game & Watch
        if (CID == 32775) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[85])));
          playcomplete(buffer);
        }
        //Rob
        if (CID == 33031) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[86])));
          playcomplete(buffer);
        }
        //Duck Hunt
        if (CID == 33287) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[87])));
          playcomplete(buffer);
        }
        //Mii Brawler
        if (CID == 49159) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[88])));
          playcomplete(buffer);
        }
        //Mii Swordfighter
        if (CID == 114695) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[89])));
          playcomplete(buffer);
        }
        //Mii Gunner
        if (CID == 180231) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[90])));
          playcomplete(buffer);
        }
        //Mewtwo
        if (CID == 38425) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[91])));
          playcomplete(buffer);
        }
        //Falco
        if (CID == 33029) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[92])));
          playcomplete(buffer);
        }
        //Lucas
        if (CID == 33058) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[93])));
          playcomplete(buffer);
        }
        //Shovel Knight
        if (CID == 49205) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[94])));
          playcomplete(buffer);
        }
        //Roy
        if (CID == 1234) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[95])));
          playcomplete(buffer);
        }
        //Ryu
        if (CID == 1234) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[96])));
          playcomplete(buffer);
        }
        //Cloud
        if (CID == 1234) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[97])));
          playcomplete(buffer);
        }
        //Corrin
        if (CID == 1234) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[98])));
          playcomplete(buffer);
        }
        //Bayonetta
        if (CID == 1234) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[99])));
          playcomplete(buffer);
        }
        //Inkling Girl
        if (CID == 65544) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[120])));
          playcomplete(buffer);
        }
        //Inkling Boy
        if (CID == 131080) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[121])));
          playcomplete(buffer);
        }
        //Squid
        if (CID == 196616) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[122])));
          playcomplete(buffer);
        }
        //Chibi
        if (CID == 49186) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[123])));
          playcomplete(buffer);
        }
        //Yarn Yoshis
        if (CID == 33620736) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[124])));
          playcomplete(buffer);
        }
        //Isabelle
        if (CID == 98561) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[125])));
          playcomplete(buffer);
        }
        //Tom Nook
        if (CID == 33537) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[126])));
          playcomplete(buffer);
        }
        //K.K. Slider
        if (CID == 33281) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[127])));
          playcomplete(buffer);
        }
        //Mabel
        if (CID == 34817) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[128])));
          playcomplete(buffer);
        }
        //Digby
        if (CID == 35841) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[129])));
          playcomplete(buffer);
        }
        //Lottie
        if (CID == 49409) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[130])));
          playcomplete(buffer);
        }
        //Cyrus
        if (CID == 35585) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[131])));
          playcomplete(buffer);
        }
        //Reese
        if (CID == 35329) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[132])));
          playcomplete(buffer);
        }
        //Blathers
        if (CID == 37377) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[133])));
          playcomplete(buffer);
        }
        //Celeste
        if (CID == 37633) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[134])));
          playcomplete(buffer);
        }
        //Resetti
        if (CID == 36353) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[135])));
          playcomplete(buffer);
        }
        //Kicks
        if (CID == 37889) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[136])));
          playcomplete(buffer);
        }
        //Timmy and Tommy
        if (CID == 1234) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[137])));
          playcomplete(buffer);
        }
        //Kapp'n
        if (CID == 1234) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[138])));
          playcomplete(buffer);
        }
        //Rover
        if (CID == 1234) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[139])));
          playcomplete(buffer);
        }
        //Wolf Link
        if (CID == 1234) 
        {strcpy_P(buffer, (char*)pgm_read_word(&(string_table[140])));
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
      lastcard = 999999999;
      currentcard = 999999998;
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
      lastcard = 999999999;
      currentcard = 999999998;
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
    PgmPrint("\n");
    return;
  }
  if (!wave.create(file)) {
    PgmPrintln("Not a valid WAV");
    return;
  }
  // ok time to play!
  wave.play();
}
