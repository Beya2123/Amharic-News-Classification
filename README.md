# Amharic-News-Classification
Amharic news classification using ontology and machine learning"
# Amharic News Ontology (ANO)

A comprehensive OWL ontology for Amharic news classification and semantic analysis. This ontology provides structured knowledge representation for Ethiopian news domains.

## 📁 Files

- `amharic-news-ontology.owl` - Main ontology file in OWL/XML format
## 🏗️ Ontology Structure

### Core Classes
- **NewsArticle** - Base class for news articles
- **NewsCategory** - Main news categories with subclasses:
  - `Politics` (ፖለቲካ)
  - `Sports` (ስፖርት)
  - `Business` (ቢዝነስ)
  - `Entertainment` (መዝናኛ)
  - `NationalNews` (ሀገር አቀፍ ዜና)
  - `InternationalNews` (አለም አቀፍ ዜና)

### Subclass Hierarchy
Each main category has specialized subclasses:
- **Politics**: Elections, Governance, ForeignPolicy, Legislation
- **Sports**: Football, Athletics, Basketball, Olympics
- **Business**: Economy, Finance, Trade, Market
- **Entertainment**: Music, Movies, Theater, Arts

### Object Properties
- `hasTopic` - Links articles to categories
- `isRelatedTo` - Defines semantic relationships
- `isPartOf` - Represents hierarchical composition
- `hasSubEvent` - Captures event relationships

### Data Properties
- `hasFrequency` - Concept occurrence tracking
- `hasDiscriminativePower` - Feature importance scoring
- `lastUpdated` - Ontology maintenance timestamp

### Individuals
187 domain-specific instances including:
- Political parties (Prosperity Party, Ezema Party)
- Sports teams (Ethiopia National Team, St. George FC)
- Business entities (Commercial Bank, Ethio Telecom)
- Entertainment personalities (Teddy Afro)
- Geographic locations (Addis Ababa, United Nations)

## 🔧 Tools for Editing

### Recommended Editors:
1. **Protégé** (Professional) - Download from [protege.stanford.edu](https://protege.stanford.edu/)
2. **WebProtégé** (Web-based) - Access at [webprotege.stanford.edu](https://webprotege.stanford.edu/)
3. **VS Code** with OWL extensions

### VS Code Extensions:
```bash
# Install these extensions:
- OWL Syntax Highlighting
- XML Tools
- RDF and OWL

# Amharic News Classification

A machine learning system that classifies Amharic news articles using ontology-based feature fusion and logistic regression.

## 🚀 Quick Start

```bash
# Install dependencies
pip install -r requirements.txt

# Train model
python main.py

# Use for prediction
from classifier import AmharicNewsClassifier
model = AmharicNewsClassifier()
model.load_model("amharic_news_classifier.pkl")
result = model.predict("Your Amharic text here")
src/
├── main.py              # Main training script
├── classifier.py        # Model class
├── preprocessor.py      # Text preprocessing
└── ontology_processor.py # Semantic features
