## Prepare the environment

```
pip install -r requirements.txt
```

## How to test the model?

1.  Download our model from `model_zoo\team08_drre\model.txt`，put it in `model_zoo\team08_drre`

2.  Download pretrained model `SD2.1` , put it in `pretrained_models/stable-diffusion-2-1-base`

3.  Modify `args.pretrained_model_path` and `args.pretrained_path` in `models\team08_drre\io.py`, please **DON'T** modify other options for best  performance 

4. Select the model 8 to test:

   ```bash
   CUDA_VISIBLE_DEVICES=0 python test.py --test_dir [path to test data dir] --save_dir [path to your save dir] --model_id 8
   ```


## How to eval the model?

```bash
CUDA_VISIBLE_DEVICES=0 python eval.py --output_folder [path to test data dir] --target_folder [path to your save dir] --metrics_save_path "./IQA_results"
```
