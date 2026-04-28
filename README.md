Akciğer Kanseri Teşhisi: Makine Öğrenmesi ile Tahmin Analizi
Proje Özeti
Bu çalışma, belirli klinik semptomlar ve yaşam tarzı faktörlerini kullanarak akciğer kanseri riskini tahmin etmeyi amaçlayan bir makine öğrenmesi projesidir. Çalışma kapsamında Lojistik Regresyon ve Rastgele Orman (Random Forest) algoritmaları kullanıp, model performansları akademik metrikler çerçevesinde karşılaştırmayı hedefledik. 
1. Veri Seti Tanımı (Data Loading)
Analiz süreci, ham verilerin Python ortamına Pandas kütüphanesi aracılığıyla entegre edilmesiyle başlattık. 
•	Veri Kaynağı: kanser.csv dosyası üzerinden DataFrame yapısı oluşturduk. 
2. Veri Ön İşleme (Data Preprocessing
•	Eksik Değer Kontrolü: df.isnull().sum() komutu ile veri setindeki eksik hücreler denetlenmiştir. 
•	Label Encoding (Etiket Kodlama): Cinsiyet (M/F) ve hedef değişken (YES/NO) gibi kategorik veriler, algoritmaların işleyebileceği 0 ve 1 sayısal değerlerine dönüştürülmüştür. 
•	Veri Tipi Düzenleme: Tüm özniteliklerin (features) sayısal veri tipinde (integer/float) olması sağlanmıştır. 
3. Özellik Seçimi ve Veriyi Bölme (Feature Selection & Splitting)
•	Bağımsız ve Bağımlı Değişkenler: LUNG_CANCER sütunu hedef değişken (y) olarak belirlenirken, diğer tüm klinik parametreler bağımsız değişken (X) olarak tanımlanmıştır. 
•	Eğitim ve Test Ayırımı: Modelin genelleme yeteneğini ölçmek adına veri seti %80 eğitim ve %20 test olacak şekilde (train_test_split) ayrılmıştır. 
4. Kullanılan Modeller ve Eğitim
1.	Lojistik Regresyon (Logistic Regression): Değişkenler arasındaki doğrusal ilişkileri modelleyen, hızlı ve yorumlanabilirliği yüksek bir sınıflandırıcıdır. 
2.	Rastgele Orman (Random Forest): Çok sayıda karar ağacı oluşturarak topluluk öğrenmesi (ensemble learning) yöntemiyle çalışan, aşırı öğrenmeye (overfitting) karşı dirençli ve güçlü bir modeldir. 
Her iki model de .fit() metodu kullanılarak eğitim verileriyle optimize edilmiştir. 
5. Performans Analizi (Evaluation)
Modellerin başarısı Karmaşıklık Matrisi (Confusion Matrix) ve çeşitli metrikler üzerinden değerlendirdik. 
Elde Edilen Bilgiler:
•	Doğruluk (Accuracy): Modeller genel toplamda %97 başarı oranına ulaştık. 
•	Duyarlılık (Recall): Kanser hastalarını doğru tespit etme oranı %98'in üzerinde çıkmıştır. Tıbbi teşhis projelerinde "yalancı negatif" oranını düşürdüğü için en kritik başarı kriteri budur. 
•	Karmaşıklık Matrisi Verileri (Her iki model için):
o	Doğru Pozitif (TP): 59 
o	Doğru Negatif (TN): 1 
o	Hatalı Pozitif (FP): 1 
o	Hatalı Negatif (FN): 1 
Sonuç
Yapılan analizler sonucunda hem Lojistik Regresyon hem de Rastgele Orman modellerinin yüksek hassasiyetle çalıştığı gözlemledik. Özellikle %98'lik duyarlılık (recall) oranı, modelin hastane ortamında kullanımında olumlu olacağını ve yüksek sonuçlar verebilceğini düşünüyoruz.
________________________________________
Kullanılan Teknolojiler
•	Dil: Python
•	Kütüphaneler: Pandas, Scikit-learn, Seaborn, Matplotlib 
•	Platform: Google Colab 


HAZIRLAYANLAR;
1-Zeynep İrem Demir
2-Rojin Acer 
3-Ayşe Kurt

