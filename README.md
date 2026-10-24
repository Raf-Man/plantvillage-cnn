# CSE 366 – Tomato/PlantVillage CNN project (Group 3)

| Notebook | Content |
|---|---|
| Submission_1_EDA_corrected.ipynb | EDA + related work (Karthik et al. row corrected) |
| Submission_2_Pretrained_Models.ipynb | MobileNetV2, ResNet-18, ShuffleNetV2, frozen vs fine-tuned |
| Submission_3_Custom_CNN.ipynb | Custom CNN from scratch (263,839 params) |
| Submission_4_CNN_with_Attention.ipynb | Same CNN + CBAM, McNemar test, 3-seed study, attention maps |

Test results (3,096 images, 64x64 input, seed 42): MobileNetV2 0.8718 -> 0.9764 (frozen -> fine-tuned), ResNet-18 0.8424 -> 0.9803, ShuffleNetV2 0.8220 -> 0.9654, custom CNN 0.9325, custom CNN + CBAM 0.9635 (3-seed mean gain +0.0085, not significant).

Run: place the Kaggle `emmarex/plantdisease` data in `archive/PlantVillage/`, `pip install torch torchvision scikit-learn pandas matplotlib scipy`, run notebooks 2-4 (CPU: ~2 h, 14 min, 1 h). Set `IMG_SIZE` in the setup cell to 128/224 on a GPU.

Push to GitHub: `git init && git add *.ipynb README.md && git commit -m "CSE 366 CNN project" && git branch -M main && git remote add origin <your-repo-url> && git push -u origin main`
