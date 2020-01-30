# tensorflow1
for tensorflow object detection



Startup instructions: 

activate virtual enviroment:
activate tensorflow1

set PYTHONPATH enviroment variable:
set PYTHONPATH=C:\tensorflow1\models;C:\tensorflow1\models\research;C:\tensorflow1\models\research\slim

cd: 
cd C:\tensorflow1\models\research\object_detection

command to train
python train.py --logtostderr --train_dir=training/ --pipeline_config_path=training/ssd_mobilenet_v2_coco.config

export inference graph:
python export_inference_graph.py --input_type image_tensor --pipeline_config_path training/ssd_mobilenet_v2_coco.config --trained_checkpoint_prefix training/model.ckpt-35218 --output_directory inference_graph

view tensorboard (training progress):
tensorboard --logdir=training
web address:
http://DESKTOP-4S7JSQP:6006/

