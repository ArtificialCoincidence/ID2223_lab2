# id2223_lab2

Author: Ruijia Dai & Zahra Khorasani Zavareh

Whisper Chinese gradio link: https://huggingface.co/spaces/ArtificialCoincidence/whisper_chinese

# What chinese_fine_tune do:
Finetune the pretrained model openai/whisper-small on Chinese dataset in mozilla-foundation/common_voice_11_0 and store the model on huggingface.

# What whisper_chinese do:
Create a gradio app to allow users to transfer microphone recorded audio/youtube video link/local video into text in Chinese.

# To run chinese_fine_tune:
requirements: Google Colab T4GPU(free version)
steps:
1. run "Prepare work" (need to paste huggingface token to login)
2. run "Load data" (need to allow colab access Google Drive to store downloaded data on drive)
3. run "Prepare Feature Extractor, Tokenizer and Data" (need to allow colab access Google Drive to store processed data on drive)
4. run "Training preparation" (need to allow colab access Google Drive to load previous stored data on drive)
5. run "Training"
6. run "Gradio"
# Note:
steps1,2,3 should run together (one right after one), steps4,5 should run together (one right after one).\
If lose GPU runtime in step5, should run step4 first next time connected to GPU.\
We suggest run steps1,2,3 first, disconnect and delete the run time, and then run steps4,5,6 to avoid running crash due to GPU RAM exceeded/not enough space in disk.
# Risk of running crash due to GPU RAM exceeded/not enough space in disk: None(if there is enough space in google drive: about 50G).
To avoid this kind of crash from happening:
1. the intermediate values such as common_voice and mapped common_voice are saved on drive so the usage of space in disk will not ccumulate during the whole running progress.
2. when mapping common voice, cache_file_names argument is added to save the cache file on drive instead of disk.
