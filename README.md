# Bachelorarbeit-BeGREIFEN
Aktueller Stand des Codes und Prototypenbau
```
// Definition der Pins für die Ventile
int valvePins[] = {3, 4, 5, 6, 7}; // Pins für die Ventile (zum Beispiel Pins 3 bis 7)

void setup() {
  // Konfiguriere alle Ventil-Pins als Ausgänge
  for (int i = 0; i < 5; i++) {
    pinMode(valvePins[i], OUTPUT);
    digitalWrite(valvePins[i], LOW); // Schalte alle Ventile zu Beginn aus
  }
}

void loop() {
  // Öffne alle Ventile
  openValves();
  delay(1000); // Halte die Ventile für 1 Sekunde geöffnet

  // Schließe alle Ventile
  closeValves();
  delay(1000); // Halte die Ventile für 1 Sekunde geschlossen
}

// Funktion zum Öffnen aller Ventile
void openValves() {
  for (int i = 0; i < 5; i++) {
    digitalWrite(valvePins[i], HIGH); // Setze den Pin auf HIGH, um das Ventil zu öffnen
  }
}

// Funktion zum Schließen aller Ventile
void closeValves() {
  for (int i = 0; i < 5; i++) {
    digitalWrite(valvePins[i], LOW); // Setze den Pin auf LOW, um das Ventil zu schließen
  }
}
```
![Prototyp Bilder](Prototyp1Bilder)
