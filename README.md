#include <iostream>
#include <iomanip>
#include <string>
#include <limits>
using namespace std;

int main()
{
    
    int jun_hp = 40;
    int jun_ap = 12;
    int jun_d = 5;
    
    int boss_hp = 400 ;
    int boss_ap = 21 ;
    int boss_d = 20 ;
    
    int turn1, turn2, turn3, turn4, turn5,
    turn6, turn7, turn8, turn9, turn10,
    turn11, turn12, turn13, turn14, turn15 ;
    int playerdamage ;
    
    bool hasRapier  = false ;
    bool hasNet = false ;
    bool hasSunglasses = false ;
    bool hasAmulet = false ;
    bool hasRustbite = false ;
    bool hasAny = false;
    bool skipbossattack = false ;
    
cout << "\x1b[1;3;31m     BLEACH: District 67 — A Text-Based Adventure \x1b[0m\n"
<<"Disclaimer: This is a fan-made educational project. Bleach is created by Tite Kubo. \n"
<<"All rights belong to their respective owners. For classroom use only.\n"
<<""
<<"You are Jun Arashi, a soul living in District 67 of Rukongai. \n"
<<"One night, a terrible presence descends — a rogue Hollow stalks the district. \n"
<<"You must prepare yourself for the coming battle. \n"
<<" \n";
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 1 — Prologue -----\x1b[0m\n";
    cout << " \n "
<< "     District 67, outskirts of Rukongai. \n"
<< " \n"
<< "Jun stands in a dark alley as screams echo through the streets. \n"
<< "The night sky trembles as a Hollow’s roar shakes the rooftops. \n"
<< "Jun clenches his fists — there is no running now. \n" ;
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 2 — The Saint (Hanae) -----\x1b[0m\n";
    cout << " \n "
<< "     Hanae, the district’s wandering saint, approaches you. \n"
<< " \n "
<< "Hanae: “You look pale, Jun. The night is cruel… let me bless you with light.” \n "
<< "Choose: \n"
<< "1. Safe — “Just a little strength will do.” (+4 ATK) \n"
<< "2. Mid — “I’ll take whatever you can give.” (+1 ATK, +1 DEF, +7 HP) \n"
<< "3. Risky — “Give me everything you have!” (+11 ATK, +3 DEF, −5 HP) \n" ;

    int scene_two ;
    cout << "Enter your choice (1,2, or 3)" ;
    cin >> scene_two ;
    cout << " \n";
    
        switch (scene_two) {
            case 1:
            jun_ap += 4 ;
            break;
            
            case 2:
            jun_hp += 7;
            jun_ap += 1;
            jun_d += 1;
            break;
            
            case 3:
            jun_hp -= 5;
            jun_ap += 11;
            jun_d += 3;
            break;
            
            default: 
            cout << "Invalid choice, defaulting to number 2 \n" ;
            jun_hp += 7;
            jun_ap += 1;
            jun_d += 1;
            break ;
        }
                cout << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "HP: " << jun_hp << "\n";
                cout << "ATK: " << jun_ap << "\n";
                cout << "DEF: " << jun_d << "\n";
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 3 — The Tinkerer (Riku) -----\x1b[0m\n";
    cout << " \n "
<< "     You find Riku, a tinkerer surrounded by scraps of strange metal. \n"
<< " \n "
<< "Riku: “You’ll need more than fists against a Hollow. I can forge something quick.” \n "
<< "Choose: \n"
<< "1. Safe — “Just give me something simple.” (+4 ATK)\n"
<< "2. Mid — “Make me sturdier.” (+1 DEF, −2 HP) \n"
<< "3. Risky — “Push the limits!” (+5 ATK, +3 DEF, −5 HP, gain Rustbite: −6 Boss DEF) \n" ;
  
    int scene_three ;
    cout << "Enter your choice (1,2, or 3)" ;
    cin >> scene_three ;
    cout << " \n";
    
        switch (scene_three) {
            case 1:
            jun_ap += 4 ;
            break;
            
            case 2:
            jun_hp -= 2;
            jun_d += 1;
            break;
            
            case 3:
            jun_hp -= 5;
            jun_ap += 5;
            jun_d += 3;
            hasRustbite = true ;
            break;
            
            default: 
            cout << "Invalid choice, defaulting to number 2 \n" ;
            jun_hp -= 2;
            jun_d += 1;
            break ;
        }
                cout << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "HP: " << jun_hp << "\n";
                cout << "ATK: " << jun_ap << "\n";
                cout << "DEF: " << jun_d << "\n";
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 4 — Sister Midori (Shrine) -----\x1b[0m\n";
    cout << " \n "
<< "     You pass a ruined shrine. Sister Midori kneels in prayer. \n"
<< " \n "
<< "Midori: “Child… I can offer a charm. But the gods ask for something in return.” \n "
<< "Choose: \n"
<< "1. Safe — “A small blessing, please.” (+4 ATK)\n"
<< "2. Mid — “I’ll take the charm.” (Gain Net, −2 HP) \n"
<< "3. Risky — “I want true power!” (+9 ATK, −4 HP) \n" ;
    
    int scene_four ;
    cout << "Enter your choice (1,2, or 3)" ;
    cin >> scene_four ;
    cout << " \n";
        
        switch (scene_four) {
            case 1:
            jun_ap += 4 ;
            break;
            
            case 2:
            jun_hp -= 2;
            hasNet = true ;
            break;
            
            case 3:
            jun_hp -= 4;
            jun_ap += 9;
            break;
            
            default: 
            cout << "Invalid choice, defaulting to number 2 \n" ;
            jun_hp -= 2;
            hasNet = true ;
            break ;
        }
                cout << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "HP: " << jun_hp << "\n";
                cout << "ATK: " << jun_ap << "\n";
                cout << "DEF: " << jun_d << "\n";
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
        
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 5 — Yumi the Smuggler -----\x1b[0m\n";
    cout << " \n "
<< "     A shadow in the corner alley beckons you. Yumi, the smuggler, grins. \n"
<< " \n "
<< "Yumi: “Dangerous times, dangerous goods. I can sell you power, if you’re willing to pay the price.” \n "
<< "Choose: \n"
<< "1. Safe — “Something reliable.” (+11 ATK)\n"
<< "2. Mid — “The Armlet of Mordiggan…” (+15 ATK, −1 DEF, −2 HP) \n"
<< "3. Risky — “What’s your strongest weapon?” (Gain Divine Rapier, −10 HP, −3 DEF, −3 ATK) \n" ;
    
    int scene_five ;
    cout << "Enter your choice (1,2, or 3)" ;
    cin >> scene_five ;
    cout << " \n";
    
         switch (scene_five) {
            case 1:
            jun_ap += 11 ;
            break;
            
            case 2:
            jun_ap += 15;
            jun_hp -= 2;
            jun_d -= 1;
            break;
            
            case 3:
            jun_hp -= 10;
            jun_ap -= 3;
            jun_d -= 3;
            hasRapier = true ;
            break;
            
            default: 
            cout << "Invalid choice, defaulting to number 2 \n" ;
            jun_ap += 15;
            jun_hp -= 2;
            jun_d -= 1;
            break;
        }
                cout << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "HP: " << jun_hp << "\n";
                cout << "ATK: " << jun_ap << "\n";
                cout << "DEF: " << jun_d << "\n";
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
    
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 6 — Kaji the Peddler -----\x1b[0m\n";
    cout << " \n "
<< "     An old peddler, Kaji, rattles his cart of bottles and charms. \n"
<< " \n "
<< "Kaji: “Spare change for power? Every blessing has a price.” \n "
<< "Choose: \n"
<< "1. Safe — “A minor boost.” (+4 ATK)\n"
<< "2. Mid — “Something stronger.” (+8 ATK, −2 HP) \n"
<< "3. Risky — “Everything you’ve got!” (+15 ATK, −2 DEF, −5 HP) \n" ;
    
    int scene_six ;
    cout << "Enter your choice (1,2, or 3)" ;
    cin >> scene_six ;
    cout << " \n";

        switch (scene_six) {
            case 1:
            jun_ap += 4 ;
            break;
            
            case 2:
            jun_ap += 8;
            jun_hp -= 2;
            break;
            
            case 3:
            jun_hp -= 5;
            jun_ap += 15;
            jun_d -= 2;
            break;
            
            default: 
            cout << "Invalid choice, defaulting to number 2 \n" ;
            jun_ap += 8;
            jun_hp -= 2;
            break;
        }
                cout << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "HP: " << jun_hp << "\n";
                cout << "ATK: " << jun_ap << "\n";
                cout << "DEF: " << jun_d << "\n";
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
        
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 7 — Aiko the Child -----\x1b[0m\n";
    cout << " \n "
<< "     Aiko, a small child, tugs at your sleeve with pleading eyes \n"
<< " \n "
<< "Aiko: “Please… help us. You’re the only one who can stand against the Hollow.” \n "
<< "Choose: \n"
<< "1. Safe — “I’ll do my best.” (+2 ATK)\n"
<< "2. Mid — “I’ll push myself harder.” (+1 ATK, +1 DEF, −1 HP) \n"
<< "3. Risky — “I’ll protect everyone at any cost!” (+8 ATK, +3 DEF, −5 HP) \n" ;

    int scene_seven ;
    cout << "Enter your choice (1,2, or 3)" ;
    cin >> scene_seven ;
    cout << " \n";
    
        switch (scene_seven) {
            case 1:
            jun_ap += 2 ;
            break;
            
            case 2:
            jun_ap += 1;
            jun_d += 1;
            jun_hp -= 1;
            break;
            
            case 3:
            jun_hp -= 5;
            jun_ap += 8;
            jun_d += 3;
            break;
            
            default: 
            cout << "Invalid choice, defaulting to number 2 \n" ;
            jun_ap += 1;
            jun_d += 1;
            jun_hp -= 1;
            break;
        }
            
                cout << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "HP: " << jun_hp << "\n";
                cout << "ATK: " << jun_ap << "\n";
                cout << "DEF: " << jun_d << "\n";
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
    
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 8 — Master Renga -----\x1b[0m\n";
    cout << " \n "
<< "     Your old mentor, Renga, leans on his cane and lowers his sunglasses. \n"
<< " \n "
<< "Renga: “Jun… take these. You’ll need sharp eyes more than a sharp blade.” \n "
<< "Choose: \n"
<< "1. Safe — “A steady path will do.” (+5 ATK)\n"
<< "2. Mid — “I’ll endure the strain.” (+7 ATK, −2 HP) \n"
<< "3. Risky — “I’ll fight with your spirit!” (Gain Sunglasses, +2 DEF, −5 HP) \n" ;

    int scene_eight ;
    cout << "Enter your choice (1,2, or 3)" ;
    cin >> scene_eight ;
    cout << " \n";
    
        switch (scene_eight) {
            case 1:
            jun_ap += 5 ;
            break;
            
            case 2:
            jun_ap += 7;
            jun_hp -= 2;
            break;
            
            case 3:
            jun_hp -= 5;
            jun_d += 2;
            hasSunglasses = true ;
            break;
            
            default: 
            cout << "Invalid choice, defaulting to number 2 \n" ;
            jun_ap += 7;
            jun_hp -= 2;
            break;
        }
            
                cout << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "HP: " << jun_hp << "\n";
                cout << "ATK: " << jun_ap << "\n";
                cout << "DEF: " << jun_d << "\n";
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
        
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 9 — Mika the Charm-Seller -----\x1b[0m\n";
    cout << " \n "
<< "     Mika holds a tray of strange charms. \n"
<< " \n "
<< "Mika: “These trinkets are cursed and blessed alike. What will you take?” \n "
<< "Choose: \n"
<< "1. Safe — “A small charm.” (+2 ATK)\n"
<< "2. Mid — “That one… it glows faintly.” (Gain Schala’s Amulet, −3 HP) \n"
<< "3. Risky — “I want the strongest one!” (+11 ATK, +2 DEF, −7 HP) \n" ;

    int scene_nine ;
    cout << "Enter your choice (1,2, or 3)" ;
    cin >> scene_nine ;
    cout << " \n";
    
        switch (scene_nine) {
            case 1:
            jun_ap += 2 ;
            break;
            
            case 2:
            jun_hp -= 3;
            hasAmulet = true ;
            break;
            
            case 3:
            jun_hp -= 7;
            jun_d += 2;
            jun_ap += 11;
            hasSunglasses = true ;
            break;
            
            default: 
            cout << "Invalid choice, defaulting to number 2 \n" ;
            jun_hp -= 3;
            hasAmulet = true ;
            break;
        }
            
                cout << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "HP: " << jun_hp << "\n";
                cout << "ATK: " << jun_ap << "\n";
                cout << "DEF: " << jun_d << "\n";
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
        
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 10 — Supply Cache -----\x1b[0m\n";
    cout << " \n "
<< "     You find a hidden cache of supplies — medicine, weapons, armor. \n"
<< " \n "
<< "Choose: \n"
<< "1. Safe — “Patch me up completely.” (Set HP to 50) \n"
<< "2. Mid — “I’ll take the sharper blades.” (+12 ATK, −3 HP) \n"
<< "3. Risky — “Load me with everything!” (+23 ATK, +2 HP) \n" ;

    int scene_ten ;
    cout << "Enter your choice (1,2, or 3)" ;
    cin >> scene_ten ;
    cout << " \n";
    
        switch (scene_ten) {
            case 1:
            jun_hp = 50;
            break;
            
            case 2:
            jun_ap += 12;
            jun_hp -= 3;
            break;
            
            case 3:
            jun_ap += 23;
            jun_hp += 2;
            break;
            
            default: 
            cout << "Invalid choice, defaulting to number 2 \n" ;
            jun_ap += 12;
            jun_hp -= 3;
            break;
        }
            
                cout << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "HP: " << jun_hp << "\n";
                cout << "ATK: " << jun_ap << "\n";
                cout << "DEF: " << jun_d << "\n";
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                
cout <<"Press any key to continue…\n" ;
cin.ignore(numeric_limits<streamsize>::max(), '\n'); 
    
    cout << " \n" ;
    cout << "\x1b[3;31m----- Scene 11 — Boss Fight: Bjorne the Rogue Hollow -----\x1b[0m\n";
    cout << " \n "
<< "     Bjorne: “Foolish soul… your resistance amuses me.” \n"
<< " \n" ;

                cout << "\x1b[3;34m----- Bjorne, The Rogue Hollow -----\x1b[0m\n";
                cout << "HP: " << boss_hp << "\n";
                cout << "ATK: " << boss_ap << "\n";
                cout << "DEF: " << boss_d << "\n";
                cout << " \n" ;

        cout << "\x1b[3;31m-----  TURN 1  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn1 ;
                switch (turn1) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                    //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }
                    
        cout << "\x1b[3;31m-----  TURN 2  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
          
            cin >> turn2 ;
                switch (turn2) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }            
                        
        cout << "\x1b[3;31m-----  TURN 3  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
         
            cin >> turn3 ;
                switch (turn3) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                     //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }      
        
        cout << "\x1b[3;31m-----  TURN 4  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
           
            cin >> turn4 ;
                switch (turn4) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                      //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }        
    
        cout << "\x1b[3;31m-----  TURN 5  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn5 ;
                switch (turn5) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                    return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                     //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }
                    
        cout << "\x1b[3;31m-----  TURN 6  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn6 ;
                switch (turn6) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                     //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }            
      
        cout << "\x1b[3;31m-----  TURN 7  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn7 ;
                switch (turn7) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                     //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }
       
        cout << "\x1b[3;31m-----  TURN 8  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn8 ;
                switch (turn8) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                     //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }
      
        cout << "\x1b[3;31m-----  TURN 9  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn9 ;
                switch (turn9) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                     //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }
      
        cout << "\x1b[3;31m-----  TURN 10  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn10 ;
                switch (turn10) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                    //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }
                    
        cout << "\x1b[3;31m-----  TURN 11  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn11 ;
                switch (turn11) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                     //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }                    
      
        cout << "\x1b[3;31m-----  TURN 12  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn12 ;
                switch (turn12) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                     //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }      
  
        cout << "\x1b[3;31m-----  TURN 13  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn13 ;
                switch (turn13) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                     //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }  
      
        cout << "\x1b[3;31m-----  TURN 14  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn14 ;
                switch (turn14) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; 
                    //status
                cout << "\n" << "\x1b[3;34m----- STATUS -----\x1b[0m\n";
                cout << "\x1b[3;34mBJORNE ---------- JUN \x1b[0m\n";
                cout << "HP: " << boss_hp  <<"----------"<< " HP: " << jun_hp << "\n" ;
                cout << "ATK: " << boss_ap <<"----------"<< " ATK: " << jun_ap << "\n" ;
                cout << "DEF: " << boss_d  <<"----------"<< " DEF: " << jun_d << "\n" ;
                cout << " \n" ;
                cout << "\x1b[3;34m----- ITEMS -----\x1b[0m\n";
                    if (hasRapier) cout << "Divine Rapier \n", hasAny = true; 
                    if (hasNet) cout << "Net \n", hasAny = true;
                    if (hasSunglasses) cout << "Sunglasses \n", hasAny = true;
                    if (hasAmulet) cout << "Schala's Amulet \n", hasAny = true;
                    if (hasRustbite) cout << "Rustbite \n", hasAny = true;
                    if (!hasAny) cout << "None\n";
                cout << "\n------------------\n";    
                    //amulate use            
                        if (jun_hp <= 0 && hasAmulet) {
                        jun_hp = 1; 
                        hasAmulet = false;
                        cout << "\n" <<  "Schala's Amulet shatters, Jun is saved at 1 HP! \n"; }
                    }      
      
        cout << "\x1b[3;31m-----  TURN 15  -----\x1b[0m\n";
        cout << " \n" ;
        cout << "Choice your action \n"
             << " \n"
             << "1. Normal Attack \n";
        if (hasRapier) cout << "2. Use Divine Rapier (275 true dmg)\n";
        if (hasNet) cout << "3. Use 90-Caliber Net (skip boss turn, still attack)\n";
        if (hasSunglasses) cout << "4. Use Sunglasses (skip boss turn, still attack)\n";
        if (hasRustbite) cout << "5. Use Rustbite Charge (-6 Boss DEF, still attack)\n";
            
            cin >> turn15 ;
                switch (turn15) {
                    
                    case 1: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                    break;    }
                    case 2: {
                        if (hasRapier) {
                            boss_hp -= 275 ;
                            hasRapier = false ;
                            cout << "\x1b[3;31m You unleash the Divine Rapier for 275 true damage! \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Rapier!\n"; }
                    break;    }
                    case 3: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You use the net and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasNet) {
                            skipbossattack = true ;
                            hasNet = false ;
                            cout << "\x1b[3;31m You entangle Bjorne with the Net! His next attack is skipped.\x1b[0m\n";
                        }
                        else { cout << "You don’t have the Net!\n"; }
                    break;    }
                    case 4: {
                        int playerdamage = max(1, jun_ap - boss_d);
                        boss_hp -= playerdamage ;
                        cout << "\x1b[3;31m You flash and slash Bjorne for " << playerdamage << " damage! \x1b[0m\n";
                        if (hasSunglasses) {
                            skipbossattack = true ;
                            hasSunglasses = false ;
                            cout << "\x1b[3;31m You flash Bjore with the Sunglasses! Bjorne’s next attack is skipped. \x1b[0m\n";
                        }
                        else { cout << "You don’t have the Sunglasses!\n"; }
                    break;    }
                    case 5: {
                        if (hasRustbite) {
                            boss_d -= 6 ;
                            hasRustbite = false ;
                            cout << "\x1b[3;31m Jun use the Rustbite — Bjorne's DEF reduced by 6 (DEF is now " << boss_d << ").\x1b[0m\n";
                            int playerdamage = max(1, jun_ap - boss_d);
                            boss_hp -= playerdamage ;
                            cout << "\x1b[3;31m You slash Bjorne after using Rustbite for " << playerdamage << " damage! \x1b[0m\n"; }
                        else { cout << "You don’t have the Rustbite!\n";}
                    break;  } 
                        
                    default: 
                         cout << "Invalid input default to normal attack.\n";
                         int playerdamage = max(1, jun_ap - boss_d);
                         boss_hp -= playerdamage ;
                         cout << "\x1b[3;31m You slash Bjorne for " << playerdamage << " damage! \x1b[0m\n" ;
                    break;
                }
                    //victory check
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    }    
                    else {
                    //taunt   
                        if (boss_hp > 300) {cout<< "\n" << "Tiny spark. I will crush you slowly. \n" ;}
                        else if (boss_hp > 200) {cout << "\n" << "You sting… nothing more. \n" ;}
                        else if (boss_hp > 100) {cout << "\n" << "Impossible… you persist?! \n" ;}
                        else cout << "\n" << "I will DEVOUR YOU! \n" ;
                    //boss atack  
                        if (!skipbossattack) {
                        int bossdamage = max(1, boss_ap - jun_d);
                        jun_hp -= bossdamage ;
                        cout << "\x1b[3;31m Bjorne attacks you for " << bossdamage << "damage!! \x1b[0m\n" ;
                        }
                        else cout << "\n" <<"\x1b[3;34m Bjorne attack is skipped in this turn! \x1b[0m\n" ;
                                skipbossattack = false ; }
                    
                    //final conclusion 
                    
                    if (boss_hp <= 0) { 
                        cout << "\n" << "Victory: Jun defeats Bjorne → shinigami arrive, Jun is recruited into the Academy." ;
                        return 0;
                    }
                    else if (jun_hp <=0 && !hasAmulet) {
                        cout << "\n" << "Defeat: Jun dies, but his stand delays Bjorne until shinigami finish it. Remembered as a hero. " ;
                        return 0;
                    } 
                    else cout << "Fatigue: Jun collapses. Shinigami arrive; the district survives. His courage becomes legend." ;              
                                
      
    return 0;
}
