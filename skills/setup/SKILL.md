---
name: setup
description: Pomáhá připojit NEMOweby ke Claude při žádostech „připoj NEMOweby“, „nastav plugin“ nebo při chybě přihlášení k NEMOwebům.
---

Pomoz uživateli připojit vlastní účet NEMOweby přes vzdálený MCP server https://www.nemoweby.cz/api/mcp. Použij OAuth přihlášení poskytované Claude. Nikdy nevyžaduj heslo, token ani ověřovací kód v chatu a nevkládej je do konfigurace.

Pokud nejsou nástroje dostupné, nasměruj uživatele do Customize → Connectors a k připojení NEMOweby. Pokud konektor chybí, pomoz přidat vlastní vzdálený konektor s uvedenou URL. Použij přihlášení OAuth; pro veřejný konektor zvol publikovanou identitu Claude (Use Claude’s published identity). Pokud nefunguje, odkaž na podporu; nepřepínej na jinou identitu kvůli získání dalších nástrojů. V organizaci může přidání konektoru vyžadovat jejího vlastníka.

Přihlašování a výběr oprávnění probíhají na webu NEMOweby. Po přihlášení proveď jeden přiměřený čtecí dotaz get_profile nebo list_properties podle oprávnění. Potvrď propojení jen tehdy, když nástroj skutečně odpověděl. Při nastavování nespouštěj změny, publikaci ani AI generování.

Pokud server odmítne účet, vysvětli skutečně vrácené omezení a odkaž na https://www.nemoweby.cz/ucet/agenti. Neměň ani neobcházej oprávnění. Instalace pluginu sama přístup neuděluje.

Vysvětli, že bez povolené samostatnosti vzniká návrh ke schválení v NEMOwebech. Samotné „ano“ v chatu ani hlasem schválení nenahrazuje. Vybrané samostatné akce lze provést pouze na zadání uživatele a v rámci oprávnění a limitů nastavených majitelem. Připojení lze odpojit na https://www.nemoweby.cz/ucet/agenti.

Doporuč první příkaz „Ukaž moje nemovitosti“. Vzdálený konektor nevyžaduje lokální server ani zapnutý počítač. Dostupnost pluginu a jeho dovedností na dalších zařízeních ověř podle aktuálního rozhraní Claude; neslibuj hlasové ovládání ani mobilní podporu bez ověření.
