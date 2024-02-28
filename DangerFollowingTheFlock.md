# ตัวอย่างการใช้งานที่ไม่ถูก

ตัวอย่างการใช้งาน P-R Curver จาก Scikit-Learn เอง

https://scikit-learn.org/stable/modules/generated/sklearn.metrics.PrecisionRecallDisplay.html#sklearn.metrics.PrecisionRecallDisplay.from_estimator
```
import matplotlib.pyplot as plt
from sklearn.datasets import make_classification
from sklearn.metrics import (precision_recall_curve,
                             PrecisionRecallDisplay)
from sklearn.model_selection import train_test_split
from sklearn.svm import SVC
X, y = make_classification(random_state=0)
X_train, X_test, y_train, y_test = train_test_split(X, y,
                                                    random_state=0)
clf = SVC(random_state=0)
clf.fit(X_train, y_train)
predictions = clf.predict(X_test)
precision, recall, _ = precision_recall_curve(y_test, predictions)
disp = PrecisionRecallDisplay(precision=precision, recall=recall)
disp.plot()
plt.show()
```

สังเกต  ค่า ```predictions``` จาก ```predictions = clf.predict(X_test)``` จะเป็น predicted class labels ซึ่ง
คำตอบมีแค่นั้น เปลี่ยนแปลงอะไรไม่ได้
แต่เอา ```predictions``` นี้ไปคำนวณ ```precision``` และ ```recall``` ต่าง ๆ จนนำไป plot P-R Curve ได้
อืมม์ ... มหัศจรรย์ ... หรือ **ทำผิด**

ดู คำอธิบายของ ```precision_recall_curve```
https://scikit-learn.org/stable/modules/generated/sklearn.metrics.precision_recall_curve.html

> The last precision and recall values are 1. and 0. respectively and do not have a corresponding threshold. This ensures that the graph starts on the y axis.
>
> The first precision and recall values are precision=class balance and recall=1.0 which corresponds to a classifier that always predicts the positive class.

นอกจากนั้นดูคำอธิบาย Parameters

> **y_true** array-like of shape (n_samples,)
> True binary labels. If labels are not either {-1, 1} or {0, 1}, then pos_label should be explicitly given.
>
> **probas_pred** array-like of shape (n_samples,)
> Target scores, can either be probability estimates of the positive class, or non-thresholded measure of decisions (as returned by decision_function on some classifiers).


นั่นคือ ตรง ```precision, recall, _ = precision_recall_curve(y_test, predictions)``` ตำแหน่งที่ใส่ ```predictions``` ควรจะใส่ predicted probability of the class ไม่ใช่ class label

![Doc](https://github.com/tatpongkatanyukul/ANN/blob/main/2024/PR_Curve.png)
