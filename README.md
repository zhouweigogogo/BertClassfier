# BertClassifier
Bert训练意图分类模型并导出onnx  
单条数据使用onnx cpu推理和使用huggingface gpu推理时间相当, 时间约为0.02s  
推理精度几乎无损

## 导出onnx
``` python
pip install optimum[exporters]
# 导出onnx模型
optimum-cli export onnx --model ./output/checkpoint-87 ./onnx/ --task text-classification
```
## onnx推理
代码详见 onnx_infer.ipynb
