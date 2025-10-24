# lisasime-whle-ts-ki-switch-case-ja-muud
```
            /* tingimuslause osad */
            if (true) { } //kaitstud sõna "if" kutsub esile tingimuslause, mille tingimus on sulgude vahel, ning millele järgneb
                              //koodiplokk tingimuse täitumisel teostatava koodiga
                else if (true) { } //kaitstud sõnad "else" ja "if" (else if) kutsuvad esile sekundaarse tingimuslause, mille tingimus
                                   //on samamoodi sulgude vahel, ning millele pepab eelnema alat kas "if" või teine "else if". Tingimuse täitumisel
                                   //ja eelneva tingimuse mittetäitumisel, teostatakse koodiploki sees olev kood.
                else { } //kaitstud sõna else kutsub esile järeltingimuse, millele peab eelnema kas "if" või "else if", ning mille koodiploki sisu
                         //täidetakse kõikide teiste "if" ja "else if" tingimuste läbikukkumisel.


            int option = 3; // -------

            switch (option) // "switch" on kaitstud sõna alternatiivse tingimuskontrolli jaoks, mida saab if-else asemel kasutada.
                            // Sulgude vahele käib muutuja nimi, mille põhjal tingimuslik ümberlülitus toimub. 
                            // Siin sulgude vahel ei ole tingimus ise, vaid kõigest kontrollitav muutuja või omakorda sulgude vahel muu tingimus.
                            // Pärast lülitusvalikut tuleb koodiplokk.
            {
                case 1:
                    // Koodiploki sees on erinevad juhtumid, juhtumit sätestatakse kaitstud sõna "case" abil.
                    // Antud juhul kontrollitakse, kas muutuja "option" on väärtus 1, millele järgneb koolon ":".
                    // Väljendades tingimuse täitumisel tehtava kooditegevuse algust.
                    break;
                // Kui tegevus on tehtud, väljutakse mitte ainult juhtumist, vaid kogu käesoleva case-tingimusblokist kaitstud
                //sõnaga "break". Peaele breaki on läuselõpumärk ";".
                //Juhtumeid võib olla mitmeid, antud juhul on neid kolm kindlalt.
                case 2:
                    break;
                case 3:
                    Console.WriteLine(option); //tehtav kooditegevus.
                    break;
                default:    //Default juhtumit täidetakse siis, kui ülejäänud juhtumid ei kirjelda muutujas "option" olevat seisu. 
                    break;  //Ka default lõppeb sõnaga break.
            }

            /* sõne tööriistad ja muud tekstiga seotut */
            string alfa = "a\nb";        // \n -> tekitab ühe sõne sisse reamurde, sõne kus on sees üks "\n", omab kahte rida.
            string beta = $"a {alfa} b"; // $ -> lubab kasutada muutjaid loogeliste sulgudega otse teks sees. On variant
                                         // formateeritud stringist.

            

                /* Tsüklid */
            // 1. do-while
            int dew = 0;
            do // "do" on kaitstud sõna, mis alustab do-while tsüklit. Pärast seda on koodiplokk {} ning ütleb et tee seda koodi
            {
                dew++;
            } while (dew != 5); //niikaua kuni while järel olevate sulgude vahel tingimus ei täitu, käivitatakse eelnev kood uuesti.

            // 2. while
            int i = 1;  //tsüklimuutuja mis aitab järge pidada while tsükli toimimisel
            while (i < 5) // "while" on kaitstud sõna mis alustab while tsükli varianti, ilma "do"-ta, ning vojab alati välist
                          // tsüklimuutuja. antud juhul on selleks i. Tsükli tingimus, mis peale "while" sõna on, asub sulgude vahel,
                          // siin kontrollitaksegi tsükli tööd, läbi kindla tingimuse kasutades tsüklimuutuja.
                          // antud juhul tsükkel töötab niikaua, kuni i on väiksem kui 5. kui i on sama suur nagu 5, siis tsükkel
                          // katkeb.
            {
                // koodiplokk kus midagi tehakse
                i++; // ning seejärel muudetakse tsüklimuutuja "i" olekut. antud juhul liidetakse 1 juurde kiirtehtega "++".
            }









            /* Loogilised tehted */


            // && -> "and" loogiline tehe, mida kasutatakse tingimuste kirjeldamisel, ning mis annab positiivse vastuse (true) juhul kui
            //       mõlemal pool "&&" märki olevad tingimused on täidetud. Kui üks neist ei ole, siis annab negatiivse vastuse (false).
            // || -> "or"! loogiline tege, mida kasutatakse tingimuste kirjeldamisel, ning mis annab positiivse vastuse (true) siis kui
            //       vähemalt üks tingimus on täidetud. Negatiivne vastus (false) tagastatakse siis, kui kõik tingimused on täitmata.
            // ! -> "not" loogiline tehe, mida kasutatakse tingimuse tulemuse inverteerimiseks. Tulemus, mis muidu tagastaks (true),
            //       hüüumärgi abil tagastab (false), ja vastupidi - tulemus mis muidu tagastaks (false), hüüumärgi abil tagastab (true)

            /* Võrdlusoperaatorid */

            // == --> "on võrdne". Võrdusmärkide ühel pool olev objekt peab vastama täpselt oma olemuselt võrdusmärkide teise pool oleva
            //         objektiga. ei ole sama nagu üks võrdusmärk, üks võrdusmärk omistab, kaks võrdleb.
            // != -> "ei ole võrdne". Võrdusmärgi ühel pool olev objekt *EI TOHI* olla samal kujul nagu võrdusmärgi teisel pool olev objekt.
            //        Ta võib olla ükskõik mis muul kujul, aga mitte võrreldava objektiga samal kujul. Võrdlusoperaator on kombinatsioon
            //        "on võrdne operaatorist, ja loogilisest tehet "not".
            // > -> "on suurem kui". Märgist vasakul pool olev objekt peaks olema suurem, kui paremal pool olev objekt.
            // < -> "on väiksem kui". Märgist vasakul pool olev objekt peaks olema väiksem, kui paremal pool olev objekt.
            // >= -> "suuremvõrdne". Märgist vasakul pool olev objekt peaks olema vähemalt võrdne või suurem kui parempoolne objekt.
            //        Võrdlusoperaator on kombinatsioon "on võrdne" ja "on suurem kui" operaatoritest.
            // <= --> "väiksemvõrdne". Märgist vasakul pool olev objekt peaks olema vähemalt võrdne või väiksem kui parempoolne objekt.
            // Võrdlusoperaator on kombinatsioon "on võrdne" ja "on väiksem kui" operaatoritest.

            /* omistusoperaatorid ja kiirtehted */

            int thing = 1;// =  -> üksik võrdusmärk omistab muutujale sisse väärtuse, mida saab kasutada läbi muutuja nime.
                thing += 1;   // += -> võrdusmärk mille ees on pluss, automaatselt liidab muutujale otsa võrdusmärgi teisel pool oleva arvu.
                              //       asendab tehet "thing = thing + 1". on kombinatsioon matemaatilisest tehetest "+" ja omistamisest "=".
                thing -= 1;   // -= -> võrdusmärk mille ees on miinus, automaatselt lahutab muutujast maha võrdusmärgi teisel pool oleva arvu.
                              // asendab tehet "thing = thing - 1". on kombinatsioon matemaatilistest tehetest "-" ja omistamisest "=".

                thing *= 2;  // *= -> võrdusmärk mille ees on korrutusmärk "*", automaatselt korrutab muutuja sisu, võrdusmärgi teisel pool oleva arvu kordi.
                             // asendab tehet "thing = thing * 2". on kombinatsioon matemaatilistest tehetest "*" ja
                             // omistamisest "=".
                thing /= 2;  // /= -> võrdusmärk mille ees on jagamismärk "/", automaatselt jagab muutuja sisu võrdusmärgi teisel pool oleva
                             // arvu osadeks. asendab tehtet "thing = thing / 2". on kombinatsioon matemaatilisest tehtest "/" ja
                             // omistamisest "=".

                thing++;      // ++ -> on spetsifiiliselt ühe juurde liitmiseks kiirtehe.
                thing--;      // -- -> on spetsifiiliselt ühe maha lahutamiseks kiirtehe.

                /* Tsüklid */
                // 1. do-while
                do // "do" on kaitstud sõna, mis alustab do-while tsüklit. Pärst seda on koodiplokk {} ning ütleb et tee seda koodi 
                {

                } while (true); //niikaua kuni while järel olevate sulgude vahel tingimus ei täitu, käivitatakse eelnev kood uuesti.

            }
        }
    } 





