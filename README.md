# apd-laborator06
### Exercițiul 1 - Verificarea frecvenței critice Nyquist (fs = 20 Hz, f_Nyquist = 10 Hz)

| f_semnal (Generator) | Condiție raportată la f_Nyquist | Frecvență aparentă în Serial Plotter | Comportament observat |
| :---: | :---: | :---: | :--- |
| **5 Hz** | `f_semnal < f_Nyquist` | **5 Hz** | Eșantionare corectă. Sinusoidă reconstituită precis (4 eșantioane pe perioadă). |
| **10 Hz** | `f_semnal = f_Nyquist` | **10 Hz** (critic) | Limita Nyquist. Doar 2 eșantioane pe perioadă; forma și amplitudinea depind critic de faza eșantionării. |
| **15 Hz** | `f_semnal > f_Nyquist` | **5 Hz** | **Fenomen de Aliasing**. Sinusoida apare falsă la 5 Hz, indistinguibilă de semnalul real de 5 Hz. |
| **20 Hz** | `f_semnal = fs` | **0 Hz** (Linie dreaptă DC) | Toate eșantioanele cad în exact același punct al fiecărei perioade, generând o valoare constantă. |
