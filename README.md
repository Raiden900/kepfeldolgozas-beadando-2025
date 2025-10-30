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

1. Papírlap detektálása a képen (szegélykeresés)
2. Perspektíva korrekció (kiegyenesítés)
3. Zajszűrés + kontrasztjavítás + binarizálás
4. Szövegfelismerés  
   - EasyOCR  
   - Tesseract OCR  
5. Pontosság mérése referencia szöveg alapján
6. Eredmények mentése

---

## ⭐ Használt technológiák

- Python 3.x
- Google Colab
- OpenCV
- EasyOCR
- Tesseract OCR
- NumPy
- Matplotlib (vizualizáció)


---

## 💡 Alkalmazott képfeldolgozási módszerek

- Dokumentum kontúr detektálása (Canny + contour keresés)
- Perspektívakorrekció (warpPerspective)
- Grayscale konverzió
- Gauss szűrés (zajszűréshez)
- Kontraszt kiemelés
- Otsu binarizáció + morfológiai tisztítás

---

## 🎯 OCR módszertan

Kétféle OCR eljárás összehasonlítása:

1) EasyOCR (beamsearch és low_text_threshold paraméterekkel)
2) Tesseract OCR (PSM 4 + OEM 1)

Mindkét módszer:
- nyers képen
- előfeldolgozott képen (binarizálás után)

Így mérve → előfeldolgozás hatása az OCR pontosságára.

---

##📊 Pontosságmérés

A felismert szöveg összehasonlítása a referencia szöveggel
→ difflib.SequenceMatcher (szöveg-hasonlóság %)

---


## 📂 Mappa szerkezet

```plaintext
project-root/
├── data/
│   ├── input/        # teszt képek (lefényképezett papírlap)
│   └── output/       # OCR eredmények + feldolgozott képek
│
├── docs/             # végleges beadandó dokumentáció (később)
├── src/              # opcionális moduláris Python kód (később)
│
├── Kepfeldolgozas_beadando.ipynb   # fő Colab notebook
└── README.md                          # projekt összefoglaló
