# 🌮 TacoConfigurator

**TacoConfigurator** is an **OWL/RDF ontology** designed to model:  
✅ **Taco ingredients** (tortillas, meats, veggies, sauces)  
✅ **Nutritional properties** (calories, price, preparation time)  
✅ **Spiciness levels** (Mild 🌶️ → Medium 🌶️🌶️ → Hot 🌶️🌶️🌶️)  

Perfect for:  
🍽️ **Digital menu systems**  
📱 **Food recommendation apps**  
🔍 **Nutritional analysis tools**

---

## 🛠️ Technical Specifications

- **Format**: OWL 2 (RDF/XML)  
- **Developed with**: Protégé 5.5.0  
- **License**: MIT  
- **SPARQL Compatible**: Yes ✅  

---

## 📂 Ontology Structure

### 🧩 Main Classes

| **Class**         | **Description**                   |
|--------------------|-----------------------------------|
| `Taco`            | Complete taco dish               |
| `TacoTortilla`    | Base (corn, flour, crunchy)       |
| `TacoFilling`     | Ingredients (meat, veggies, sauces) |
| `Spiciness`       | Heat scale (Mild/Medium/Hot)      |

### 🔗 Key Properties

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
