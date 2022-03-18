# Introduccion_deep_learning
Apuntes y código correspondientes al curso INTRODUCCION AL DEEP LEARNING MIE820

Primero tenemos que hacer un ambiente virtual y esto lo podemos hacer con anaconda o instalando la libreria virtualenv.

>>pip install virtualenv

>>virtualenv name_venv

Activamos el ambiente virtual:

>>name_venv\Scripts\activate

Para desactivar el ambiente virtual:

>>deactivate

Una vez dentro del ambiente virtual, podemos instalar las librerias necesarias:
**En el caso de tensorflow y pytorch, para poder ocupar la gpu, primero debemos instalar cuda, de manera opcional cudnn(numpy con esteroides).**
Para instalar tensorflow, keras y jupyter:

>>pip install -r requirements.txt

Para instalar pytorch:

>>pip install torch==1.10.0+cu113 torchvision==0.11.1+cu113 torchaudio==0.10.0+cu113 -f https://download.pytorch.org/whl/cu113/torch_stable.html

Podemos probar que pytorch y tensorflow tengan acceso a la gpu con las siguientes lineas de codigo:

tensorflow: 
>>import tensorflow as tf
>>tf.test.gpu_device_name()

pytorch:
>>import torch
>>torch.cuda.is_available()
