# 🌮 TacoConfigurator

**TacoConfigurator** è un'**ontologia OWL/RDF** progettata per modellare:  
✅ **Ingredienti dei tacos** (tortillas, carni, verdure, salse)  
✅ **Proprietà nutrizionali** (calorie, prezzo, tempo di preparazione)  
✅ **Livelli di piccantezza** (Mild 🌶️ → Medium 🌶️🌶️ → Hot 🌶️🌶️🌶️)  

Perfetto per:  
🍽️ **Sistemi di menu digitali**  
📱 **App di raccomandazione alimentare**  
🔍 **Strumenti di analisi nutrizionale**

---

## 🛠️ Specifiche Tecniche

- **Formato**: OWL 2 (RDF/XML)  
- **Sviluppato con**: Protégé 5.5.0  
- **Licenza**: MIT  
- **Compatibile con SPARQL**: Sì ✅  

---

## 📂 Struttura dell'Ontologia

### 🧩 Classi Principali

| **Classe**       | **Descrizione**                     |
|-------------------|-------------------------------------|
| `Taco`           | Piatto completo di taco            |
| `TacoTortilla`   | Base (mais, farina, croccante)      |
| `TacoFilling`    | Ingredienti (carne, verdure, salse) |
| `Spiciness`      | Scala di piccantezza (Mild/Medium/Hot) |

### 🔗 Proprietà Chiave

```mermaid
graph LR
  Taco --hasTortilla--> Tortilla
  Taco --hasFilling--> Filling
  Filling --hasSpiciness--> Spiciness
```

🚀 Getting Started
Clone the repository:

bash
Copy
git clone https://github.com/riccardoimaninoobar/TacoConfigurator.git
Open in Protégé:

Download Protégé

File → Open → TacoConfigurator.rdf

Run sample SPARQL queries:

sparql
Copy
# Find all vegetarian tacos
SELECT ?taco WHERE {
  ?taco a :Taco .
  FILTER NOT EXISTS { ?taco :hasFilling ?filling .
                     ?filling a :MeatFilling }
}
📊 Example Data
Taco Type	Calories	Price	Spiciness
MexicanTaco	790kcal	€8.25	Medium
DiabloTaco	560kcal	€6.25	Hot
KidsTaco	1020kcal	€6.75	Mild

## License
This ontology is released under the [MIT License](LICENSE).  
Copyright (c) 2025 Riccardo Imani Noobar.
