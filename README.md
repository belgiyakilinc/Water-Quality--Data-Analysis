# Water-Quality-Data-Analysis

**Genel Bakış:**
Bu proje, bir Su Kalitesi veri setinin Keşifçi Veri Analizi (EDA) ve tahmine dayalı modellemesine odaklanmaktadır. Temel amaç, pH, Sertlik, Toplam Çözünmüş Katı Madde, Kloraminler, Sülfat, İletkenlik, Organik Karbon, Trihalometanlar ve Bulanıklık gibi çeşitli kimyasal ve fiziksel özelliklere dayanarak suyun `Potability` (İçilebilirlik / insan tüketimi için güvenli olup olmadığı) durumunu tahmin etmektir.

**Temel Adımlar:**
1.  **Veri Keşfi ve Görselleştirme:** Özelliklerin dağılımı ve aralarındaki korelasyonlar incelendi. Hedef değişken (`Potability`) ve özellik dağılımları Plotly ve Seaborn kullanılarak görselleştirildi.
2.  **Veri Ön İşleme:** `ph`, `Sulfate` ve `Trihalomethanes` sütunlarındaki eksik değerler ilgili ortalamalarla doldurularak giderildi. Ardından veri seti eğitim ve test setlerine ayrıldı ve Min-Max normalizasyonu kullanılarak ölçeklendirildi.
3.  **Modelleme ve Değerlendirme:** Karar Ağacı Sınıflandırıcısı (Decision Tree) ve Rastgele Orman Sınıflandırıcısı (Random Forest) eğitildi. Performansları kesinlik (precision) skorları ve karmaşıklık matrisleri (confusion matrix) kullanılarak değerlendirildi.
4.  **Hiperparametre Ayarı:** Daha iyi tahmin performansı için Random Forest modelinin hiperparametrelerini optimize etmek amacıyla Tabakalı K-Katlamalı (Stratified K-Fold) çapraz doğrulama ile `RandomizedSearchCV` uygulandı.

---
**Overview:**
This project focuses on the Exploratory Data Analysis (EDA) and predictive modeling of a Water Quality dataset. The main goal is to predict the `Potability` of water (whether it is safe for human consumption) based on various chemical and physical attributes such as pH, Hardness, Total Dissolved Solids, Chloramines, Sulfate, Conductivity, Organic Carbon, Trihalomethanes, and Turbidity.

**Key Steps:**
1.  **Data Exploration & Visualization:** Analyzed the distribution of features and their correlations. Visualized the target variable (`Potability`) and feature distributions using Plotly and Seaborn.
2.  **Data Preprocessing:** Handled missing values in `ph`, `Sulfate`, and `Trihalomethanes` columns by filling them with their respective means. The dataset was then split into training and testing sets and scaled using Min-Max normalization.
3.  **Modeling & Evaluation:** Trained a Decision Tree Classifier and a Random Forest Classifier. Evaluated their performance using precision scores and confusion matrices. 
4.  **Hyperparameter Tuning:** Applied `RandomizedSearchCV` with Stratified K-Fold cross-validation to optimize the hyperparameters of the Random Forest model for better predictive performance.



