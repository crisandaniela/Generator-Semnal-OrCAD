# Generator de Semnal Triunghi-Dreptunghi (OrCAD PSpice)

## 📖 Descriere Proiect
Acest proiect constă în proiectarea, dimensionarea și simularea unui generator de semnal capabil să genereze simultan forme de undă triunghiulare și dreptunghiulare. Astfel de circuite sunt utilizate frecvent în telecomunicații, circuite de testare și sisteme de achiziție de date. 

## ⚙️ Specificații Tehnice
* **Tensiune de Alimentare:** Simetrică la ±16V.
* **Domeniu de Frecvență:** Reglabil în intervalul 11 kHz – 25 kHz.
* **Amplitudine Semnal Triunghiular:** Ajustabilă între 4 V și 8 V.
* **Amplitudine Semnal Dreptunghiular:** Ajustabilă între 2 V și 10 V.

## 🧠 Arhitectura Circuitului
Montajul este implementat folosind un singur circuit integrat **TL084** (conținând 4 amplificatoare operaționale), ceea ce simplifică schema și reduce numărul de componente. Structura de bază folosește o buclă închisă compusă din două etaje:
1. **Integrator Inversor:** Transformă semnalul dreptunghiular de la intrare într-un semnal triunghiular la ieșire prin integrarea curentului.
2. **Trigger Schmitt Neinversor:** Cu reacție pozitivă, detectează nivelurile de tensiune și comută rapid ieșirea.
*Notă: Pentru reglarea amplitudinilor independent de frecvență, au fost adăugate divizoare rezistive cu potențiometru și buffere.*

## 📊 Simulări și Analize (OrCAD PSpice)
Pentru validarea ecuațiilor matematice și testarea fiabilității au fost rulate următoarele simulări:
* **Analiză Transient (Domeniul Timp):** Vizualizarea formelor de undă și confirmarea amorsării oscilațiilor.
* **Analiză Parametrică:** Validarea funcționării potențiometrelor pentru baleierea corectă a frecvenței și limitelor de tensiune.
* **Analiză Worst Case:** Determinarea deviațiilor în cel mai nefavorabil mod de însumare a abaterilor componentelor.
* **Analiză Monte Carlo (50 rulări):** Demonstrează că deviațiile (distribuție Gauss) sunt ținute sub control de rețeaua de reacție, chiar și folosind rezistențe cu toleranță de 5%.

## 📂 Conținutul Repository-ului
* `Crisan_Diana_Daniela_2121.pdf` - Documentația tehnică completă a proiectului. Conține toate calculele de dimensionare, schemele electrice și graficele simulărilor extrase din PSpice. *(Recomand vizualizarea directă în browser)*.
