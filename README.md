# 🎬 Retrieval-Augmented Generation (RAG) for Movie Plot Question Answering
This project implements a Retrieval-Augmented Generation (RAG) pipeline using a pre-trained model from Hugging Face to answer questions based on movie plots from the Wikipedia Movie Plot Dataset.

# 🚀 Features
✅ Load and preprocess movie plot data
✅ Generate embeddings using all-MiniLM-L6-v2
✅ Implement efficient retrieval using FAISS (cosine similarity)
✅ Use distilbert-base-uncased-distilled-squad for question answering
✅ Answer user queries based on relevant movie plots

# 📂 Dataset
Dataset: Wikipedia Movie Plot Dataset
We use a subset of this dataset to create a knowledge base of movie plots.

# 🛠 Installation

1️⃣ Clone the repository:
bash
Copy
Edit
git clone https://github.com/yourusername/rag-movie-plots.git
cd rag-movie-plots

2️⃣ Install dependencies:
bash
Copy
Edit
pip install -r requirements.txt

3️⃣ Download the dataset:
Place the CSV file in the project directory.

# 📜 Usage

🔹 Step 1: Preprocess the dataset
Run the following script to clean and preprocess movie plots:
bash
Copy
Edit
python preprocess.py

🔹 Step 2: Generate embeddings & create FAISS index
bash
Copy
Edit
python create_index.py

🔹 Step 3: Ask questions!
bash
Copy
Edit
python query.py --question "What is the plot of Inception?"

# 🔧 How It Works
1️⃣ Preprocessing: Loads the dataset, extracts relevant columns, and cleans text.
2️⃣ Embedding Generation: Uses all-MiniLM-L6-v2 to convert plots into vector embeddings.
3️⃣ Retrieval (FAISS): Finds the most relevant movie plots for a given query using cosine similarity.
4️⃣ Question Answering: The retrieved text and query are passed to distilbert-base-uncased-distilled-squad for answer generation.

📌 Example
Query:
bash
Copy
Edit
python query.py --question "What movie is about dreams within dreams?"
Output:

vbnet
Copy
Edit
Movie: Inception (2010)
Answer: A thief enters people's dreams to steal secrets and gets caught in a dream within a dream.

# 📚 Dependencies
transformers
sentence-transformers
faiss
pandas
torch
Install them via:

bash
Copy
Edit
pip install -r requirements.txt
🤖 Model Details
Retrieval Model: all-MiniLM-L6-v2 (efficient sentence embeddings)
QA Model: distilbert-base-uncased-distilled-squad (pre-trained on QA tasks)

# 💡 Future Improvements
✅ Expand dataset for better generalization
✅ Improve retrieval with advanced ranking techniques
✅ Implement a web-based interface for easier interaction

# 🔥 Contributions Welcome! Feel free to submit issues or PRs.
📧 Contact: surajkamlapuri123@gmail.com
