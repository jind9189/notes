git clone https://github.com/ysharma3501/LuxTTS.git

uv pip install --cache-dir d:\python-cache-dir -r requirements.txt



#Kokoro-82M-WBUI
--cache-dir d:\python-cache-dir pip
kokoroonnx -
 CLI based tool, update script_01.py with required text prompt and execute command. it supports hindi language also.
```
	python script_01.py
```





# install cuda environment for GTX 1650

mkdir cuda
cd cuda
uv venv --python 3.12
uv pip install  --cache-dir d:\python-cache-dir pip
uv pip install  --cache-dir d:\python-cache-dir torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

pip install k2


# Installation of Kokoro-82M-WebUI

pip install  --cache-dir d:\python-cache-dir -r requirements.txt
pip install  --cache-dir d:\python-cache-dir scipy torch munch transformers phonemizer librosa pydub 
python app.py
http://192.168.1.11:9000/


# PAckage ohfpiper 
cd d:\aisetup_2/ohfpiper
scrip\activate
pip install  --cache-dir d:\python-cache-dir  piper
