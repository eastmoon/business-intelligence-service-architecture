# 演算服務架構 ( Calculate Service Architecture )

本專案原稱為 Computer vision play，原本設計之初是想整合常見的電腦視覺演算法，並基於 Pipe & Filter 架構的概念撰寫一個專用於 C/C++ 或 Python 的軟體架構，並運用於嵌入式系統中或邊緣運算設備；然而，考量近年的產業變化與演算軟體演進，重新自系統層面審視對於影像處理、樣式識別、電腦視覺等基礎知識，皆回歸於特徵工程、機械學習、人工智慧等新一代詞彙。

對此，將專案重新定位為演算服務架構 ( Calculate Service Architecture )，並從系統運用層面規劃架構，考量其用途著眼於以下幾個要點：

+ 演算法的容器化編譯、執行、封裝，讓演算法運用如 [SaaS](https://zh.wikipedia.org/zh-tw/%E8%BD%AF%E4%BB%B6%E5%8D%B3%E6%9C%8D%E5%8A%A1) 或 [FaaS](https://en.wikipedia.org/wiki/Function_as_a_service)
+ 設計單元應包括
    - 主要語言，C/C++、Python
    - 服務單元，資料解析、演算法、資料彙整、報表產生
    - 演算框架，OpenCV、OpenVINO、Scikit-Learn、Tensorflow
    - 系統單元，Console pipeline executor、Jenkins、Elasticsearch-Logstash-Kibana

原始專案的設計目的，則回歸到[資料流架構](https://github.com/eastmoon/dataflow-architecture)設計，其運用的分野則需視對於演算法的計算量、效率而調整。

## 介紹 ( Introduction )

![calculate-service-layer-architecture](doc/img/calculate-service-layer-architecture.png)

## 文獻

+ [雲端運算 IaaS、PaaS、SaaS 與 FaaS](https://cynthiachuang.github.io/Difference-between-IaaS-PaaS-SaaS-and-FaaS/)
+ Image processing
    - [Image processing wiki](https://zh.wikipedia.org/wiki/%E5%9B%BE%E5%83%8F%E5%A4%84%E7%90%86)
    - [IPOL Journal · Image Processing On Line](http://www.ipol.im/)
    - [Image processing online tutorials](http://www.imageprocessingplace.com/root_files_V3/tutorials.htm)
    - [Digital Image procesing](https://www.youtube.com/playlist?list=PLZ9qNFMHZ-A79y1StvUUqgyL-O0fZh2rs)
    - [Image Processing online demo](http://felixniklas.com/imageprocessing/)
    - [Basic Image Processing Demos](http://robotics.eecs.berkeley.edu/~sastry/ee20/)

+ Computer vision
    - [Machine learning coursera](https://www.youtube.com/watch?v=qeHZOdmJvFU&list=PLZ9qNFMHZ-A4rycgrgOYma6zxF4BZGGPW)
    - [What is an Image Processing Framework for Machine Learning?](https://www.iguazio.com/glossary/image-processing-framework/)

+ Machine learning
    - [Top 15 Machine Learning Frameworks for Machine Learning Experts](https://intellipaat.com/blog/machine-learning-frameworks/)
