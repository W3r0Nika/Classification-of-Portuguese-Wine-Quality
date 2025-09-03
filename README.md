# Predykcja jakości wina – analiza danych i modele klasyfikacyjne w R

## Opis projektu
Celem projektu jest stworzenie modelu predykcyjnego, który na podstawie cech fizykochemicznych win typu **Vinho Verde** przewiduje ich ocenę jakościową (od 0 do 10). Projekt obejmuje pełny proces analizy danych, przygotowania zmiennych, budowy i tuningu modeli klasyfikacyjnych w języku **R**.

## Zbiór danych
- **Źródło:** [Wine Quality Dataset na Kaggle](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset)  
- **Liczba próbek:** 1143  
- **Typ wina:** czerwone Vinho Verde  
- **Zmienna docelowa:** `quality` (ocena jakości wina)  
- **Zmienne wejściowe:** `fixed.acidity`, `volatile.acidity`, `citric.acid`, `residual.sugar`, `chlorides`, `free.sulfur.dioxide`, `total.sulfur.dioxide`, `density`, `pH`, `sulphates`, `alcohol`

## Analiza danych
- Sprawdzenie braków danych i ich uzupełnienie  
- Analiza rozkładów zmiennych oraz korelacji z jakością wina  
- Identyfikacja wartości odstających (outliers) metodą **IQR**  
- Transformacja **Yeo-Johnson** w celu poprawy rozkładu zmiennych  
- Oversampling klas niedoreprezentowanych w zbiorze treningowym

## Metody
Testowano różne algorytmy klasyfikacyjne:
- **Regresja logistyczna**  
- **Drzewo decyzyjne (Decision Tree)**  
- **Las losowy (Random Forest)**  
- **XGBoost (Boosted Tree)**  
- **Naive Bayes**  
- **SVM (Support Vector Machine)**  
- **KNN (K-Nearest Neighbors)**  

Do strojenia hiperparametrów wybrano trzy najlepsze modele: **Random Forest**, **XGBoost** oraz **SVM**.  

## Wyniki
- Najlepsze wyniki uzyskały modele **Random Forest** i **XGBoost** pod względem dokładności (**Accuracy**) i stabilności predykcji  
- Model **SVM** lepiej radził sobie z klasyfikacją rzadziej występujących klas, osiągając wyższy **F1 Score**  
- Niezbalansowanie klas stanowiło wyzwanie dla wszystkich modeli

## Wnioski
- Zaawansowane modele (Random Forest, XGBoost) poprawiają skuteczność predykcji jakości wina w porównaniu do prostych modeli  
- Klasy niedoreprezentowane wymagają dodatkowych technik balansowania danych  
- Cecha fizykochemiczne, takie jak zawartość alkoholu czy lotna kwasowość, mają istotny wpływ na ocenę jakości wina
