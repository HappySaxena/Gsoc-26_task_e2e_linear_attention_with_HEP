# GSoC 2026 ML4SCI Evaluation Task 🚀
**Linear Attention Vision Transformers for End-to-End Mass Regression and Classification**

This repository contains the code and experiments for the official evaluation task for the Google Summer of Code (GSoC) 2026 project under the **ML4SCI** umbrella. 

The objective of this task is to explore and benchmark linear-complexity attention mechanisms (**XCiT** and **L2ViT**) on High Energy Physics (HEP) event reconstruction, specifically focusing on self-supervised pretraining on unlabelled CMS data and multi-task supervised fine-tuning for particle classification and invariant mass regression.

---

## 📦 Pretrained Model Weights
> **Note:** Due to GitHub's file size limitations, all optimized model weights (`.pth` files) for the pretraining, from-scratch, and fine-tuned phases have been hosted externally.

🔗 **[https://drive.google.com/drive/folders/1T3Da11_HxaJqT6IqGhoGBZitWelOcfil?usp=drive_link]** 

To run inference or resume training, please download the respective weights from the Drive link above and place them in the root directory or update the weight paths inside the notebooks.

---

## 📂 Repository Structure

The project is divided into two primary architectural approaches. Each approach contains modular Jupyter Notebooks for every phase of the training pipeline (Pretraining, Training from Scratch, and Fine-tuning).

```task 
specific_task_2h/
├── Approach1_xcit/
│   ├── Results_images/                         # Contains loss curves, ROC plots, and mass resolution graphs
│   ├── xcit-image-transformer_pretraining.ipynb # Self-supervised pretraining (MIM) on unlabelled data
│   ├── xcit-scratch-mass-only.ipynb            # Supervised training from scratch (Mass + Classification)
│   ├── xcit-scratch-mass_momentum.ipynb        # Supervised training from scratch (Mass + Momentum + Class)
│   ├── xcit_finetuned_mass_only.ipynb          # Fine-tuning pretrained XCiT (Mass + Classification)
│   └── xcit_finetuned_mass_momentum.ipynb      # Fine-tuning pretrained XCiT (Mass + Momentum + Class)
│
├── Approach2_l2vit/
│   ├── Result_images/                          # Contains loss curves, ROC plots, and mass resolution graphs
│   ├── l2vit_pretrain.ipynb                    # Self-supervised pretraining (MIM) on unlabelled data
│   ├── l2vit-from-scratch_mass_only.ipynb      # Supervised training from scratch (Mass + Classification)
│   ├── l2vit-from-scratch_mass_momentum.ipynb  # Supervised training from scratch (Mass + Momentum + Class)
│   ├── l2vit_finetuned_mass_only.ipynb         # Fine-tuning pretrained L2ViT (Mass + Classification)
│   └── l2vit_finetune_mass_and_momentum.ipynb  # Fine-tuning pretrained L2ViT (Mass + Momentum + Class)
│
├── .gitattributes
├── .gitignore
└── README.md
