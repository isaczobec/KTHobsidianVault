för at interacta med *peripherals* = devices som är externa till datorn

memory mappede IO = specefika adresser man skriver till och från för att skicka/läsa data till peripherals

har en adress decoder som hittar rätt device och enablar writes när man utfärdar en write/read insturction; hittar rätt IO device

GPIO kan läsa och skriva till, sätta direction of pins
GPIO shared med special purporse peripherals ibland, kan behöva configuration registers för att konfigurera detta och interupts om det är en input pin