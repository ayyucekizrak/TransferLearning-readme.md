📌[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ayyucekizrak/Udemy_DerinOgrenmeyeGiris/blob/master/TransferOgrenme_FineTuning/Fine_Tune_TransferOgrenme.ipynb) **Google Colab Not Defteri**

📌[![Open In Jupyter](https://github.com/jupyter/notebook/blob/master/docs/resources/icon_32x32.svg)](https://nbviewer.jupyter.org/github/ayyucekizrak/Udemy_DerinOgrenmeyeGiris/blob/master/TransferOgrenme_FineTuning/Fine_Tune_TransferOgrenme.ipynb) **Jupyter Not Defteri** 
---
# Fine-Tuning ve Transfer Öğrenme Nedir?
Fine-Tuning and Transfer Learning 👽


---
Bir kuşun öğrendiklerini size aktarabildiğini düşünün ya da sizin öğrendiklerinizi bir balığa, kulağa çılgınca geliyor değil mi? 
Ya da şöyle diyelim ben bir bardağı tanımak için atalarımdan bu yana ve doğduğumdan beri öğrendiğim basit özellikler var (kenar, köşe, şekil, maddesel yapısı vb.) bunlardan yola çıkarak hiç görmediğim bardakları ya da hiç görmediğim bazı nesnelerin bardak olmadığına dair kararlar veriyorum. Yalnızca bu bilgiyi öğrenen bir makinenin bildiğiklerini başka bir makineye transfer edip tekrar öğrenme sürecini atlamasıdır desem! Neyse hadi başlayalım 😊

 **Bilgisayarlı görü problemi üzerinden yola çıkalım ancak birçok veri ve problem tipi için uygulanabilecek bir yöntemden bahsediyorum. Öyle ki bir veri kümesi var sizin tanımak istediğiniz nesne de içinde var ancak veri seti çok büyük (bu harika bişey 😃) model de çok başarılı (e bu da harika 🤗) ama sizin o modeli o veri kümesi için eğitmeniz günler belki haftalar alacak. Gerçi burda eğitilmişi var!** 🧐 
 

---
 
 ![](https://a4.pbase.com/o4/98/367898/1/59218520.tn_Braintransferwatercolor.jpg)
 
 
 
Bir yapay öğrenme modelinin öğrendiklerinden faydalanarak yeni bir problemi çözüyorsunuz. Öğrendiklerinin tamamını ya da bir kısmını transfer ederek bu işlemi gerçekleştiriyorsunuz. Tam da bu yüzden adı **Transfer Öğrenme**. Bazen sadece kendi modeliniz için basit özelliklerin öğrenilmesi için ayarlamalar yapıyorsanız bu kez adı **Fine-Tuning** oluyor. Bir başka versiyonu da örneğin verinizde _Golden_ ve _Husky_ cinsinde köpekler ve _Kadın_, _Erkek_ bireylerden oluşan insan görselleri var. Siz burada model ile **Köpek-İnsan** sınıflandırması yapabileceğiniz gibi **Kadın-Erkek** ya da **Golden-Husky** sınıflaması da yapabilirsiniz ki bu versiyonun adı da **Çoklu Öğrenme (Multi-Task Learning)** olarak isimlendirilir. Son konuya bir başka _Pazar Çalışması_ nda yer vereceğim. 
 
![](https://github.com/ayyucekizrak/TransferLearning_FineTuning/blob/master/TL_FT.png)

---

🎯 **1. Versiyon:** Yalnızca bu parametreleri model için kullandığımızda test işlemini yaparak yeni bir sinir ağı tasarımı yapmayız. Tüm eğitilmiş modeli test için kullanabiliriz. Özellikle mobil ve gerçek zamanlı öğrenme gerektirmeyen uç noktada çalışacak sistemlerde bu yöntem uygulanmaktadır. Belli periyotlarla eğitim işlemi daha geniş verilerle tekrarlanıp sistem performansı artırılabilir.


🎯 **2. Versiyon:**  Eğitilmiş modelin bir kısmını alıp devamında veri kümesinde bulunmayan kendi problemimize ait veriler için eğitiriz. Böyle yaptığımızda Paratmetre hesabı yani işlem yükünü azaltmış oluyoruz ve zamandan da kazanmış oluyoruz. Aynı zamanda kendi problemimiz için verilerimiz kısıtlı olsa dahi bu yöntemle büyük veri setlerinde öğrenilen temel öznitelikler açısından da daha yüksek bir başarıya ulaşılmış olur. Fakat bu yöntemi uygularkan de dikkat etmemiz gereken stratejiler var. 

> * Kullanacağımız veri önceden eğitilen modelin veri kümesiyle ne kadar benzer ya da farklı

> *  Kullanacağımız verinin büyüklüğü

Aşağıdaki şema ile nasıl bir tercihte bulunabileceğimizi basit bir şekilde belirleyebiliriz.


![](https://github.com/ayyucekizrak/TransferLearning_FineTuning/blob/master/TL_FN2.png)


 🕵 So let's look at a simple example of how we can use a test process that we can run edge!

### 🔥For this purpose, ResNet50 was trained with deep neural networks for the IMAGENET dataset and weight parameters were recorded at the end of the training.

---
⚡️[On **Algorithmia** you can make your own model available to everyone as an API.
With the **ResNet** deep learning model trained on the **ImageNe**t dataset, you can try the image classification algorithm free of charge from the link below. Thanks to **Yavuz Kömeçoğlu** for this work.](https://algorithmia.com/algorithms/yavuzkomecoglu/ImageClassification)
![](https://github.com/ayyucekizrak/Udemy_DerinOgrenmeyeGiris/blob/master/TransferOgrenme_FineTuning/Algortihma.jpg)

---
 ✏️ **Use the links below for more resources:**

[Comparison of Activation Functions for Deep Neural Networks](https://towardsdatascience.com/comparison-of-activation-functions-for-deep-neural-networks-706ac4284c8a)

[Step-by-Step Use of Google Colab’s Free TPU](https://medium.com/deep-learning-turkiye/ad%C4%B1m-ad%C4%B1m-google-colab-%C3%BCcretsiz-tpu-kullan%C4%B1m%C4%B1-621dc6e5487dhttps://heartbeat.fritz.ai/step-by-step-use-of-google-colab-free-tpu-75f8629492b3)

---

 ### ⭐️[Transfer learning with TensorFlow Hub](https://www.tensorflow.org/tutorials/images/hub_with_keras)⭐️
 ### ⭐️ [Transfer learning from pre-trained models](https://towardsdatascience.com/transfer-learning-from-pre-trained-models-f2393f124751)⭐️
