# Robotic Vision: YOLOv8 Object Detection

## Deskripsi Proyek
Repositori ini berisi hasil eksperimen *transfer learning* menggunakan arsitektur model **YOLOv8 Nano (yolov8n)** untuk keperluan sistem *robotic vision*. Model ini dilatih agar ringan, cepat, dan optimal saat diimplementasikan pada perangkat keras robotika.

## Informasi Dataset
Dataset yang digunakan berjumlah 120 gambar yang dianotasi dan diekspor ke dalam format YOLOv8 untuk mendeteksi objek terkait.

## Metrik Evaluasi & Pelatihan
Model telah dilatih menggunakan Google Colab selama 50 *epochs* dan file bobot terbaiknya disimpan sebagai `best.pt`.

## Cara Menggunakan Model (Inferensi)
Untuk menguji model `best.pt` pada gambar baru, gunakan skrip Python berikut:

```python
from ultralytics import YOLO

# Memuat model yang sudah dilatih
model = YOLO('best.pt')

# Melakukan prediksi objek
results = model.predict('test_image.jpg', save=True)
