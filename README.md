# Family In the Park: 
A realistic (image)[https://github.com/galiakraicheva/ai_image_generation/blob/main/family_in_the_park/ComfyUI_temp_kpoeh_00001_.png] of a couple in the park, generated with ComfyUI with this (Workflow)[https://github.com/galiakraicheva/ai_image_generation/blob/main/family_in_the_park/task_2_comfyui_00006_image_edit.json]

### Step 1: Generating the image

1. Prompt Used

- Positive Prompt: A realistic photo of a man and woman outdoors in a park during sunset. The man has short brown hair, he is 40 years old, wearing a casual blue shirt and jeans. The woman has long blonde hair, wearing a white dress. She is 35 years old. She is holding flowers at one hand and a bag in the other. They are surrounded by lush greenery and a glowing sunset in the background. High detail, soft lighting, photorealistic style, ultra-realistic skin textures, and natural poses. RAW photo, dslr, Fujifilm XT3, film grain
- Negative Prompt: ugly, deformed, deformed iris, deformed puplis, semi-realistic, cgi, 3d, sketch, cartoon, anime, UnrealisticDream

2. Model used: (Realistic Vision V6)[https://civitai.com/models/4201/realistic-vision-v20]
3. VAE Encoder: (ClearVAE 2.3)[https://civitai.com/models/22354/clearvaesd15]

4. Image resolution: 768 x 1024 

5. KSampler Parameters: 60 steps, cfg 7 (maybe that is one of the reasons why there is no bouquet but a single flower), denoise 1 (a new fully random image), DPM++ 2M Karras (good for photorealism)

6. Problems with initial image: mainly the holding hands but also if you zoom in, the eyes and the woman's teeth may improve. 

### Step 2: Fixing the hand problem (to some extend)

1. Prompt:
-Positive Prompt: perfect hands, two hands holding each other, professional photography
-Negative Prompt: distorted fingers, UnrealisticDream, disformed fingers
2. Models used: (ControlNet HandRefiner Pruned) [https://huggingface.co/hr16/ControlNet-HandRefiner-pruned/blob/main/control_sd15_inpaint_depth_hand_fp16.safetensors]
MeshGraphormer Hand Refiner

### Further steps: 
- test other models too (Epic Realism, DreamShaper, SD-XL 1.0, which I tried to download but the refiner model's page gave Internal Error)
- improve the eyes


