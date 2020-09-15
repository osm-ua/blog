---
layout: "post"
title: "Моніторинг території з автоматичними сповіщеннями про правки в Telegram"
date: "2020-09-15 16:20"
lang: uk
ref: "monitoring-with-osmcha-telegram"
---


Думаю багато хто з маперів хоче моніторити зміни на певній території (наприклад рідне місто, район проживання тощо) на предмет вандалізму чи просто слідкувати за правками інших маперів. Ідеально ще й отримувати про це сповіщення в найбільш зручному місці.
  

Далі коротка інструкція, як я це реалізував за допомогою двох сервісів – [Osmcha](https://osmcha.org/) і [IFTTT](http://ifttt.com).

  
  

![](https://lh4.googleusercontent.com/Lab_w2Or8NpX1x2LAo_Mbciiou1QqsN0Zd1L35cezFy-ovVcGPqf17Q3Yf5r1fPkONHmg5ZmxR0tBLzn6g3kasAE25rktNculn6LLbz4T3p0Hw19wpeMMzIddUXitzTSJHDOE1xP)

- Налаштовуємо фільтр в OSMcha
    

  

![](https://lh5.googleusercontent.com/O_th_vMHy0gyTYdZkM1P5GsE-YWYYzpnuk8SVe8TF_ffcUSmim7ul7BFnA5zEpi3Y-4pOIWlBWCXiSOEL2lFakV8-2OKjpaF7N_YOGkxtgu_lt6ysmMWaUp-5rGJAICoVVyI7o7J)

  

- Спочатку полігоном позначаємо потрібну територію моніторингу
    
- BBox size bound вказую або 1 або 2, це для того, щоб сюди потрапляли лише правки в межах конкретного виділеного поля, а не як в History на головній osm.org.
    

  

![](https://lh5.googleusercontent.com/EAMBH8OwhNTmjZ3g95tX-Lrujcb3FiTiA-FtQ3dLuDJzIYPv4TskDGxMybTAM-55FDe-fg6l-Qyvqd1MS_CPZGKMSeofUkfRlPEGk6AxmbU9oJjc6T69No4SK6kWkIYTJVfXo_Wb)

- Коли всі параметри фільтрування вказані – зберігаємо фільтр.
    

  

![](https://lh3.googleusercontent.com/ShqFA_5de0ZZTzGRS63wf6U3qnqObrHlHCv0gPGdfxbJuFTpUH_bpGhup5u6G9upbVQWV6XhO6YPYUeUxQbxjZZwKWvkVFBxGFDfgBdoz0aUO2ABlhEKzFXIHin3Ytwn7q6V2YqI)

- Пишемо довільну назву для фільтра
    

![](https://lh3.googleusercontent.com/oAMdO7GBhLRAXKUkl8sjizxPzTNimiaiallMHY8dzZYen6y8zDE_MojE1zq7KYmietiPULBCc1JuRqAKNXvTyeoR6Jk6Rk2Qg-zJZzkRZSzLccbt2mN8qoPEUUYgeaaFPyJsX96F)

- Для кожного фільтра генерується окрема rss-стрічка. її URL копіюємо. Він нам пригодиться далі для IFTTT.


Далі переходимо у сервіс [IFTTT](https://ifttt.com/), який допоможе нам зв’язати все з Телеграмом.


- Створюємо новий recipe
    

![](https://lh4.googleusercontent.com/X6dYEe6BJymDM0VvITfq5eQ37STRYG-G5uI6iMqSHx9CCANXJvd3V6BIZfQdT18CVK4Gw31yEv0HgEbKTcOZcn-L0-KrtvHwqHw8ctvJ1QSV4THA-qMYj_ajE4Mgw8VI-1qXkob_)

- Тут шукаємо RSS і вибираємо пункт New feed item

![](https://lh3.googleusercontent.com/hStfC9Z-L6xwuiEaeSGQ7D__eZfCuy84oEdVWvduSAbyx6vJcWFjlb0OFBYn4gDliMC8OauEDqM-NdSHN_bqLSwswANVmXSkuuNj2djHLvTPWeAWsCk__nth-5BOAjfizmQ0rRZB)

![](https://lh5.googleusercontent.com/xAAHHC7UxEEQL1Jvu3ih8I2HOBCTGazGm9yNpiySE6bx2UKHEuUTLBiKmuMiHfsWdZn-_5hzaY_z9QmUWYH5M745TY-ZzD7FDmPtx66E2tkNBFMYyvo3B7-aBk2HeWALZooukvJM)


  - Тут вставляємо URL RSS стрічки з Osmcha
  - Створюємо триггер

![](https://lh6.googleusercontent.com/wGJzcKXhaEr8T4sKEDXsOtlGOfdGR_dKq1ho1khIyeD8uz5jf8eANVPhDLa3D8Syd9XXRcSGDrd9Ux2UtTfhvwPPXZayNKhM_hy1ieksMPUfkShui1l548A0QSwOMh9z1-JqBMCF)

 - Далі треба додати Телеграм і вибрати пункт Send message


![](https://lh4.googleusercontent.com/Q4VqVEO8unkgAHX5xpykDOSRXWNWIjuVVLzYNttbpzBmMe21PJVCJDRdAOZEeRnLvTZMCgHBSzViRaEbrAcSGi03uKDc8JlkIpdsK_2l9Ahn_6iZXnpI5zR8HwFLADGVtVvG_VXH)


  

![](https://lh6.googleusercontent.com/YVfXe-yUV8jkyljfkBK8iElNL39sJCGTAZnkqPeUC5oue3VWvhl_NUx85pwTvwjQFDErrhcgFzfb0nJYS7tOvGYHsHit_s2QYHtrcdnn3sAC00X4ORiumypIInkpO-R0y5d8oYcT)

- Далі залишаємо стандартні налаштування і тиснемо Create action.

![](https://lh6.googleusercontent.com/enrFNrVk3ILKrubq3cH6ciF7e2tPI5CzwAe6A3g1cwbTMdUL1WIH4_budtA7CuGqgZpfKtyfSjprvswTQOnxalXWhn8JRcaiM84iu-lF_5b-7vlyS_uidxGEsT3eWWMPv853lATu)

Це в принципі все з налаштувань. Клікаєте далі по тому як веде вас IFTTT.

Вже зовсім скоро (якщо будуть зміни мапи звісно) вам будуть приходити в месенджер отакого вигляду повідомлення.

  

![](https://lh4.googleusercontent.com/nSEM7ppFkdW5ZfF7HDZv-0k8dPBw_0wRFR4SD8WXHzQ0DvBGgVQxU-pnrkRn4XysQPr7Fm0o1eJSvpOCdgqO4TEReBuoJ-GJtyK-VUC4bhI6OxOcMV_hP0R85HNMxB3BfXghRiT3)
