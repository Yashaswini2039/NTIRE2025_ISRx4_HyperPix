# NTIRE 2025 Challenge on Image Super-Resolution (x4): Hiperpix

## Environment
- [PyTorch >= 1.7](https://pytorch.org/) *(Do NOT use torch 1.8! It may cause abnormal performance.)*

## Installation
### Run the following commands:

```bash
pip install -r requirements.txt
```
If basicsr is installed, you can uninstall it by running the following command:
bash
pip uninstall basicsr -y

### Open models/team26_DAT/HAT_SRx4_ImageNet-LR.yml and modify the following lines:
- line no. 15: dataroot_lq [insert the input path of the low-quality images]
- line no. 42: pretrain_network_g [insert the path of the pretrained model]
- line no. 45: results_root [insert the path of the result folder]
- line no. 47: visualization  [insert the path of the result folder] (keep both results_root same as visualization)

### Run the testing script:
```bash
python test.py --test_dir <path to low quality img folder> --model_id 26
```
(if encounter any error ignore it and run eval.py script)

### Run the eval scrip:
```bash
python eval.py --output_folder <saved images of the previous script> --target_folder <gt high res images> 
```
