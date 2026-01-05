# TRVZB_Z2M
Sonoff TRVZB Heizungssteuerung für Home Assistant / Zigbee2MQTT

Blueprint für Home Assistant, der Sonoff TRVZB Heizkörperthermostate über Zigbee2MQTT steuert, dabei aber möglichst viele native Funktionen des TRV nutzt.
​
Der Wochenplan wird aus einem einzelnen HA‑Schedule direkt als weekly_schedule_* ins Thermostat geschrieben, der Auto‑Modus läuft vollständig im Gerät.
​

Funktionen:
​

Zeitprogramm im TRV: Komfort‑ und Absenktemperaturen werden aus dem Schedule in den internen Wochenplan des TRVZB übertragen (AUTO‑Modus).
​

Fenster‑Erkennung: Fenstergruppen in HA → Fenster auf = Heizung AUS (system_mode off), Fenster zu = zurück in AUTO.
​

Anwesenheit: Home/Away‑Schalter, die zwischen Komfort‑ und Eco‑Plan umschalten, indem der Wochenplan im TRV neu geschrieben wird.
​

Externer Temperatursensor (optional): Raumfühler kann als Quelle genutzt werden, dessen Temperatur wird als external_temperature_input ins TRV gespiegelt.
​

Mitternachts‑Reset: setzt TRVZB täglich um 00:00 Uhr zurück auf AUTO, um manuelle Overrides am Gerät sauber in den Plan zurückzuführen.
​

Ziel des Projekts ist eine robuste, weitgehend autarke Heizungsregelung im Thermostat selbst, bei gleichzeitig komfortabler Bedienung über Home Assistant und Zigbee2MQTT.
​
