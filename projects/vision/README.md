# vision
　画像解析を専門に行うプロジェクト

使用している PC のカメラを使ってノートブックからリアルタイムカメラビューを実装したい場合は **[display_video.ipynb](display_video.ipynb)** をみてください。別のプロジェクトにリアルタイムカメラビューを実装したい場合は、以下のモジュールと関数を実装するとできる。<br>
　以下のように関数`show`に画像データを代入する。

> [!CAUTION]
> この関数が1度実行されると、Jupiter Notebook が起動している間 **常にカメラがバックグラウンドで起動し続けます。**

```python
# 必要なモジュール
from io import BytesIO
from PIL import Image
import IPython
import os

# 実装関数
def show(img, fmt='jpeg'):
    f = BytesIO()
    Image.fromarray(img).save(f, fmt)
    IPython.display.display(IPython.display.Image(data=f.getvalue()))
    IPython.display.clear_output(wait=True)

######## 実装例 #########
# opencv
import cv2

cap = cv2.VideoCapture(0)
assert cap.isOpened(), 'Could not open video device'

try:
    while(True):
        ret, frame = cap.read()
        if ret:
            frame = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
            show(frame)

except KeyboardInterrupt:
    cap.release()
    print('Stream stopped')
```
