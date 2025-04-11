# Детекция и сегментация огня и дыма с YOLOv8  

## **Датасет**  
- FLAME + кастомные данные (YOLO-разметка)  
- Ссылка: [Yandex Disk](https://disk.yandex.ru/d/_GkMswJZaPtqvg)  

## **Модель**  
- **YOLOv8** (детекция + сегментация)  
- Обучение: 50 эпох, аугментация (HSV, blur, rotation)  

## **Метрики**  
| Объект  | Precision | Recall | mAP50 |  
|---------|----------|--------|-------|  
| Огонь   | 0.72     | 0.65   | 0.63  |  
| Дым     | 0.82     | 0.81   | 0.79  |  

## **Скорость**  
- YOLOv8n: 45 FPS  
- YOLOv8s: 28 FPS  

## **Использование**  
```python
from ultralytics import YOLO  
model = YOLO("best.pt")  
results = model.predict("input.jpg")  


## Git не пропускает большую моель, нужно развернуть локально! Папки появяться в ходе выполнения кода. Результат в папке runs
