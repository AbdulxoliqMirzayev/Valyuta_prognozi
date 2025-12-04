# USD/UZS Valyuta Kursini Bashorat Qilish (ARIMA Modeli)

Ushbu loyiha O‘zbekiston so‘mi (UZS) va AQSH dollari (USD) o‘rtasidagi valyuta kursini tarixiy ma’lumotlar asosida bashorat qilish uchun yaratilgan. Loyiha vaqt qatori (Time Series) statistikasiga asoslanadi va **ARIMA(1,1,1)** modeli yordamida **2025-yil 5–12 dekabr kunlari uchun 7 kunlik forecast** beradi.

##  Loyiha maqsadi

- USD/UZS valyuta kursini tahlil qilish
- Tarixiy narxlar asosida kelajakdagi 7 kunlik bashorat olish
- Modelni matematik metrikalar bilan baholash
- ARIMA modelining real ishlash mexanizmini ko‘rsatish
- Natijani grafik ko‘rinishda taqdim etish

##  Model qanday ishlaydi?

### Ma’lumotlarni tayyorlash
- Sana formatlari to‘g‘rilanadi  
- Bo‘sh kunlar (weekend/holiday) forward-fill bilan to‘ldiriladi  
- Kunlik chastotaga o‘tkaziladi  
- Narxlar stasionarlik uchun tekshiriladi (ADF)

###  Stasionarlikni yaxshilash
- d=1 differensiyalash qo‘llanadi  
- ACF va PACF grafiklari orqali p va q parametrlari tanlanadi  

### Modelni o‘qitish

model = ARIMA(train, order=(1, 1, 1))
model_fit = model.fit()
 
Tarixiy narx line chart

Bashorat qilingan narx (qizil rangda)

7 kunlik Moving Average

ACF va PACF grafiklari (ARIMA parametrlari uchun)

Grafiklar modelning vaqt bo‘yicha o‘zgarishini va bashoratning qanchalik barqaror ekanini ko‘rsatadi.
kelajakda bu modelni yanada takomillashtirish real time malumotlar asosida narxlarni bashorat qiluvchi model qilsak bo'ladi. 

### NATIJALAR 

<img width="586" height="209" alt="image" src="https://github.com/user-attachments/assets/d34536cd-5473-412a-8c56-0403035a3835" />

### MODELNI ANIQLIGI 
<img width="379" height="109" alt="image" src="https://github.com/user-attachments/assets/a056e815-f46f-47f3-97ff-6d5a4aec8aa7" />

