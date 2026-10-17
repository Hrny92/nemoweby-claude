# NEMOweby pro Claude

Spravujte vlastní nemovitosti a poptávky v NEMOwebech přímo z Claude. Ptejte se na ceny, čtěte relevantní podklady, připravujte úpravy webů a ověřujte stav schválených změn. Plugin obsahuje dvě dovednosti a jeden vzdálený MCP konektor. Vyžaduje aktivní účet NEMOweby a udělení oprávnění jeho majitelem. Nenahrazuje předplatné a neodemyká placené funkce.

## Připojení

1. V Claude otevřete Customize → Plugins → Add → Upload plugin a vyberte balíček `nemoweby.plugin`. V katalogu jej vyhledejte až po potvrzeném zveřejnění.
2. Připojte konektor NEMOweby. Pro veřejnou integraci použijte OAuth a **Use Claude’s published identity**.
3. Na webu NEMOweby se přihlaste vlastním účtem, zkontrolujte e-mail a vyberte potřebná oprávnění.
4. Pro první test stačí čtení profilu a nemovitostí. Napište „Ukaž moje nemovitosti a jejich ceny.“

Bez pluginu lze přidat vlastní konektor v Customize → Connectors → Add custom connector s adresou **https://www.nemoweby.cz/api/mcp**. Přímé připojení nezahrnuje přibalené dovednosti. V Team/Enterprise může konektor nejprve povolovat správce. Pro veřejnou integraci neměňte publikovanou identitu Claude na generického klienta. Při chybě se obraťte na podporu.

Podrobný veřejný návod po nasazení: https://www.nemoweby.cz/napoveda/claude.
Vzdálené MCP nepotřebuje lokální server, zapnutý počítač, vlastní AI klíč ani proměnné prostředí. Hesla, tokeny a ověřovací kódy nikdy neposílejte do chatu.

## Příklady použití

- „Ukaž moje nemovitosti a jejich ceny.“
- „Shrň moje nové poptávky.“
- „Připrav návrh změny ceny vybrané nemovitosti na 5 290 000 Kč.“
- „Ověř stav posledního návrhu.“

## Oprávnění a změny

Každý uživatel připojuje pouze vlastní účet. Přístup k účtům, které spravuje pro jiné makléře, se automaticky nepřenáší. Server ověřuje vlastnictví každé položky i aktuální oprávnění. Ve výchozím stavu změny vytvoří návrh ke schválení na https://www.nemoweby.cz/ucet/agenti. Majitel může pro každé připojení povolit vybrané samostatné akce s limity. Výslovná žádost o návrh čeká vždy; mazání a změny přístupů se schvalují vždy. Samotné „ano“ v chatu schválení nenahrazuje.

Veřejná integrace Claude nespouští AI generování obrázků, retuší, vizualizací, propagačních grafik, videa ani audia a neprodává digitální balíčky. Existující podklady lze číst s příslušným oprávněním. Generování je dostupné přímo v aplikaci NEMOweby mimo tento konektor.

## Soukromí

Konektor předává Claude pouze vyžádané údaje v udělených oblastech, například profil, nabídky, osobní kontakty v poptávkách nebo podklady webů. Data zpracovává také Anthropic podle účtu a podmínek uživatele. Plugin nemá vlastní lokální úložiště ani další MCP cíle. NEMOweby uchovávají data účtu a návrhy v rámci služby; přehled připojení, návrhů a aktivity je dostupný majiteli. Odpojení zneplatní přístup, samo nesmaže účet ani záznamy již zpracované poskytovatelem Claude.

[Ochrana osobních údajů](https://www.nemoweby.cz/gdpr) · [Podmínky služby](https://www.nemoweby.cz/obchodni-podminky) · [Správa a odpojení](https://www.nemoweby.cz/ucet/agenti)

Podpora a bezpečnostní hlášení: info@hrncirovistudio.cz. Neposílejte hesla ani tokeny.

## Zdroj a licence

Licence MIT platí pouze pro soubory tohoto pluginu, nikoliv pro server NEMOweby, službu, data nebo ochranné známky. Plugin obsahuje `setup`, `sprava-nemowebu` a vzdálený server `nemoweby`. Neobsahuje spustitelné programy, lokální MCP, hooky ani další závislosti.

Pro lokální načtení rozbalené složky v Claude Code použijte `claude --plugin-dir ./nemoweby`. Autorizaci otevřete přes `/mcp`. Pro kontrolu použijte `claude plugin validate ./nemoweby`.
