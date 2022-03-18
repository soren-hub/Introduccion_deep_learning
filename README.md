# Introduccion_deep_learning
Apuntes y código correspondientes al curso INTRODUCCION AL DEEP LEARNING MIE820

Primero tenemos que hacer un ambiente virtual y esto lo podemos hacer con anaconda o instalando la libreria virtualenv.

>>pip install virtualenv

>>virtualenv name_venv

Activamos el ambiente virtual:

>>name_venv\Scripts\activate

Para desactivar el ambiente virtual:

>>deactivate

Podemos descargar el codigo del curso con el siguiente comando (se debe tener git instalado): 
Abrimos git y ejetamos:

>>git clone https://github.com/soren-hub/Introduccion_deep_learning.git

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

Para comparar las ventajas de ocupar la gpu, podemos usar el siguiente comando en jupyter:

>>import torch
>>dev = torch.device("cuda") if torch.cuda.is_available() else torch.device("cpu")
#con cpu
>>%%time
>>torch.rand(100000000)

#con gpu
>>%%time
>>torch.rand(100000000,device=dev)

Nota: Si se corre el codigo por primera vez puede que la cpu corra más rapido debido a que no se ha inicializado la gpu.
Pero una vez que la gpu este bien iniciada, el codigo se ejecutará mas rapido.

El codigo correspondiente a la libreria pytorch estara en la rama "translate-torch", para ver este codigo dentro de la carpeta descargada al hacer el git clone, tenemos que abrir git y ejecutar:

>>git checkout translate-torch

Ahora si abrimos cualquier archivo de jupyter podemos ver el codigo implementado en pytorch:
**ESTO AUN ESTA EN DESARROLLO**

Para regresar a la version del codigo en tensorflow, tenemos que ejecutar:

>>git checkout main 






