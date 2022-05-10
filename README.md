# IoT_Jalan
Mengukur getaran di jalanan dengan menggunakan Phyphox dan klasifikasi kendaraan yang lewat dengan Fuzzy Logic bersama Jose Vernando.

## Milestone 1 - Pengukuran dan Plot
![image](https://user-images.githubusercontent.com/57952404/167529082-97106b86-83f5-415c-936b-5c5344385495.png)

### Pengambilan Data
- Pengambilan data kendaraan menggunakan aplikasi Phyphox dengan sensor linear accelerometer dengan frekuensi sampling 100 Hz pada maksimum resolusi 16g.
- Pengambilan data dilakukan selama 4  menit atau 240 detik.
- Visualisasi cara pengambilan data kendaraan

### Plot
![image](https://user-images.githubusercontent.com/57952404/167531024-35c53b25-e219-4e19-b0a4-8c095414718e.png)

![image](https://user-images.githubusercontent.com/57952404/167531055-b02b318c-2757-4833-b0d1-38e56c0779f1.png)

## Milestone 2 - FFT dan Signal Filtering

### FFT (Fast Fourier Transform)
Menggunakan algoritma fft dari Scipy dengan range 0-35 Hz
![image](https://user-images.githubusercontent.com/57952404/167531075-ad0d5c31-0ac7-4218-8c2d-d8dc2f294403.png)

### Filtering
Dengan menggunakan Band Pass Filter. Hasil pengukuran setelah filtering
![image](https://user-images.githubusercontent.com/57952404/167531092-ab7f44ed-ee91-48bb-bfa4-46bb022bdb2b.png)

Hasil FFT setelah filtering
![image](https://user-images.githubusercontent.com/57952404/167531106-b6dd9c66-1d7a-4994-a716-c5ecabc5ca2e.png)

## Milestone 3 - Kemampuan Cerdas dengan Fuzzy Logic
Memilih 2 sumbu relevan, yaitu sumbu Y dan sumbu Z
![image](https://user-images.githubusercontent.com/57952404/167530882-05bd612e-ec5d-4a6f-80b2-e812b8e586ab.png)

Membership Function Sumbu Y

![image](https://user-images.githubusercontent.com/57952404/167530837-c5f44081-ce1e-4cdf-88b8-edc6e4f94c1d.png)

Membership Function Sumbu Z

![image](https://user-images.githubusercontent.com/57952404/167530911-851c77bb-4914-4dae-8eb6-fc940e602491.png)

Fuzzy Rule / Inference

SumbuY | SumbuZ | Output
--|--|--
YTinggi | ZTinggi | Truk
YTinggi | ZSedang | Mobil
YTinggi | ZRendah | Mobil
YSedang | ZTinggi | Mobil
YSedang | ZSedang | Mobil
YSedang | ZRendah | Motor
YRendah | ZTinggi | Mobil
YRendah | ZSedang | Motor
YRendah | ZRendah | Motor

Deffuzification Takagi-Sugeno

![image](https://user-images.githubusercontent.com/57952404/167531199-8e55e503-9d77-4f45-ab6b-9b71ecfcc398.png)

## Output
![image](https://user-images.githubusercontent.com/57952404/167531685-3ee37725-cd38-4b64-bbdb-98c45454cfb6.png)

## Presentasi
Untuk file presentasi ada di IoT Presentasi.pptx dan video nya ada di : https://drive.google.com/drive/folders/1Vg5aCdMd6sSivqszWe1mMRjm8E-BCf1N?usp=sharing
