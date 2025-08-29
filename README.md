# 🎤 Vosk STT Project

This project is a **Speech-to-Text (STT)** system built using the **Vosk** library. It supports both **real-time (streaming)** and **offline (non-streaming)** processing.  

## 🚀 Technologies Used
- [Vosk](https://alphacephei.com/vosk/) – Speech recognition model (**vosk-model-small** is used for faster performance)  
- [noisereduce](https://pypi.org/project/noisereduce/) – Noise reduction to improve **latency**  
- [jiwer](https://pypi.org/project/jiwer/) – Calculates **WER (Word Error Rate)** and **CER (Character Error Rate)**  
- [matplotlib](https://matplotlib.org/) – Visualization of results  
- [numpy](https://numpy.org/) – Numerical computations  

---

## 📂 Project Structure
Vosk_STT.py # Real-time STT (microphone → text)
 - Vosk_STT.py # Real-time STT + Latency calculation
 - WER_CER_Latency.py # Offline STT + WER/CER/Latency calculation
 - test_set/ # Test audio files (WAV format)
 - expected.json # Manually written expected results for each test file
 - predicted.json # Transcript prediction of model


## ⚡ Functionality
1. **Real-time STT (Vosk_STT.py)**  
   - Captures audio from the microphone  
   - Applies `noisereduce` for noise removal  
   - Uses the `vosk small` model for live speech-to-text  
   - Calculates **latency** for each audio block  

2. **Offline STT (WER_CER_Latency.py)**  
   - Reads WAV files from the `test_set` folder  
   - Compares transcriptions with manually written references in `expected.json`  
   - Computes **WER** and **CER** using `jiwer`  
   - Visualizes results with `matplotlib`  
   - Calculates **latency** for each file  

---

This project is designed for experimenting with speech recognition performance and evaluation.
Using vosk-model-small provides faster execution, while noise reduction helps optimize latency.

<img width="1851" height="760" alt="image" src="https://github.com/user-attachments/assets/6ff580ab-593b-4073-b9e9-8a41da3ab1aa" />
<img width="1033" height="589" alt="image" src="https://github.com/user-attachments/assets/38216d7e-4e42-4469-a01b-50003cbc9eb0" />
