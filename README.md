**TensorFlow Lite en Raspberry Pi 4**  
Lo modelos mejor optimizados que fueron encontrados para funcionar sin GPU, en una Rpi4 de 4GB.

**Clonar el repo:**  
git clone https://github.com/jorgevespa/tflite_rpi.git

**Acceder al directorio:**  
cd tflite_rpi

**Instalar VirtualEnv:**  
pip3 install virtualenv

**Crear el ambiente virtual:**  
python3 -m venv tflite_rpi-env

**Activar el ambiente virtual:**  
source tflite_rpi-env/bin/activate

**Instalar los requerimientos:**  
sudo chmod +x get_pi_req.sh  
bash get_pi_req.sh

**Correr el script:**  
python3 TFL_object_detection.py --modeldir=object_detection

**Opciones:**  
Es posible cambiar los modelos del directorio "modelos" en el paramtero --modeldir  
face_mask_v2: Detector de barbijo (Promedio 2.7 FPS)  
object_detection: Detector de objetos (Promedio 4.2 FPS)  
ssd_mobilenet_v3_small: Detector de objetos (Promedio 4.7 FPS)  

Es posible usar una camara IP con RTSP (Comentar linea 22/Descomentar linea 23):
self.stream = cv2.VideoCapture('rtsp://admin:admin@PUBLIC_IP:554/0')
