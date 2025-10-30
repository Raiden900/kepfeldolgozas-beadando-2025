# Képfeldolgozás beadandó – 2025

### Téma
Kézzel írott papírlap digitalizálása: dokumentum detektálás, torzítás javítása, binarizálás, majd OCR felismerés (EasyOCR + Tesseract).

### Hallgató
- **Név:** Velekey Ádám  
- **Neptun:** H3Q42Y  
- **Tárgy:** GKLB_INTM152 – Képfeldolgozás  
- **Fejlesztési környezet:** Google Colab + Python + OpenCV  
- **Státusz:** 1. konzultáció – működő prototípus kész (2025.10)  

---

## 🧠 Projekt célja

Egy lefotózott papírlap automatikus feldolgozása:

1. Papírlap detektálása képen (szegélykeresés)
2. Perspektíva korrekció (kiegyenesítés)
3. Zajszűrés + kontrasztjavítás + binarizálás
4. Szövegfelismerés
   - EasyOCRx
   - Tesseract OCR
5. Pontosság mérése referencia szöveg alapján
6. Eredmények mentése



## 📂 Mappa szerkezet




project-root/
├── data/
│   ├── input/        # teszt képek (lefényképezett papírlapok)
│   └── output/       # OCR eredmények + feldolgozott képek
│
├── docs/             # végleges beadandó dokumentáció (később)
├── src/              # opcionális moduláris Python kód (később)
│
├── Kepfeldolgozas_beadando.ipynb   # fő Colab notebook
└── README.md         # projekt összefoglaló

