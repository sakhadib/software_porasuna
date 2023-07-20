# বিশেষ গ্রাফ

>[Adib Sakhawat](https://sakhawatadib.com) <br>
> Tags: Algorithm, graph <br>
>Date: July 19, 2023



" তুমি তো কেবলি ছবি <br>
পটে আঁকা "

এহেম গ্রাফের ক্ষেত্রে সবই তো গ্রাফ। এখানে ভেদাভেদ বৈষম্য কি না করলেই হত না ? আসলে বৈষম্য করা হয় নাই। গ্রাফ দেখে যেন চেনা যায়, বা কাজে সুবিধা হয় এজন্য এসব গ্রাফ-জাতিগোষ্ঠী গুলোকে নাম দেওয়া হয়েছে।

## **কমপ্লিট গ্রাফ**

যখন কোন গ্রাফ এর **প্রত্যেকটি নোড অন্য সকল নোডের সাথে একটি ইউনিক এজ এর মাধ্যমে যুক্ত থাকে** তখন তাকে কমপ্লিট গ্রাফ বলে। যদি কোন গ্রাফে n টি নোড থাকে আর n টি নোড ই একে অন্যের সাথে কানেক্টেড হয় তাহলে একে বলে, $K_n$ । তাহলে নিচের গ্রাফটিকে আমরা $K_4$ গ্রাফ বলতে পারি।

![https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-1@2x.png](https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-1@2x.png)

## **সাইকেল গ্রাফ**

কোন গ্রাফ যদি এমন হয় যে, যেকোন নোড থেকে যাত্রা শুরু করলে সবগুলো নোড একবার অতিক্রম করে আবার প্রথম নোড এ ফিরে আসা যায় তবে তাকে বলে সাইকেল গ্রাফ। যেমন নিচের গ্রাফগুলো সাইকেল গ্রাফ,

![https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-2@2x.png](https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-2@2x.png)

![https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-3@2x.png](https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-3@2x.png)

![https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-4@2x.png](https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-4@2x.png)

## **হুইল গ্রাফ**

কোন সাইকেল গ্রাফে যদি এমন কোন নোড থাকে যা অন্য সকল নোডের সাথে যুক্ত তবে ঐ গ্রাফকে বলে হুইলগ্রাফ। নিচের ছবিটি একটি হুইলগ্রাফের। কারন এখানে ‘গ’ নোড অন্য সকল নোডের সাথে যুক্ত হয়েছে আর এইটা যে সাইকেল গ্রাফ তা তো আগেই দেখেছি। ঐ সকলের সাথে যুক্ত নোডের ডিগ্রি n হয় তাহলে ঐ গ্রাফকে $W_n$ বলা হয়। এই ক্ষেত্রে নিচের গ্রাফটি $W_4$

![https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-4@2x.png](https://sakhawatadib.com/wp-content/uploads/2023/07/4-spcl-4@2x.png)