# Owl-E-Journaling-App-using-Llama-3.2-model
Description: AI-assisted journaling app using LLaMA 3.2, Unsloth, and Flutter with privacy-first design.
Link for the Journaling APP
https://drive.google.com/file/d/1gz2orEP-jXUX-Vh5_OugMfx9gEXry5s8/view?usp=sharing

DhiWise is used as UI interface so no use of flutter was required and coversion of Figma to Flutter was also done by DhiWise.

Owl-E-Journaling-App/
├── README.md
├── LICENSE
├── .gitignore
├── docs/
│   └── Project_Report.pdf
├── design/
│   └── figma_screenshots/
├── frontend/
│   ├── flutter_app/
│   └── pubspec.yaml
├── backend/
│   ├── ollama_config/
│   └── inference_server.py
├── model/
│   ├── lora_weights/
│   └── training_notebook.ipynb
├── data/
│   └── prompts_and_responses.json
├── assets/
│   ├── mood_music/
│   └── icons/
└── references/
    └── academic_papers.md
A GPU-supported machine (for model inference)

Flutter installed: https://docs.flutter.dev/get-started/install

Ollama installed: https://ollama.com/download

Python ≥ 3.10 (for model training/LoRA)

 Run LLaMA Model Locally via Ollama
 Code:
 # Pull base LLaMA model
ollama pull llama3

# Merge with LoRA weights (optional step depending on training)
ollama run llama3

Or, if you have a finetuned model:
ollama create owl-e -f Modelfile
ollama run owl-e

 Run the Flutter App
cd frontend/flutter_app
flutter pub get
flutter run
