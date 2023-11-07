# SQLi_cheatsheet

<b>SQL injection cheat sheet<b/>

<h1>SQL injection nədir ?</h1>

SQL injection istifadəçinin məlumat daxil etməsi üçün nəzərdə tutulmuş hissələrdə(sorğularda) SQL verilənlər bazasına aid kodların daxil edilməsi və bu kodların SQL verilənlər bazasında icra olunmasına deyilir.

SQL injection 3 qrupa ayrılmaqla 5 yerə bölünür:

1.UNION BASED         2.ERROR BASED          3.BOOLEAN BASED       4.TIME BASED   5.OUT-OF-BAND

![image](https://github.com/azar-malikov/SQLi_cheatsheet/assets/103067933/2f49cbb6-780c-482f-be9a-43d72c4fc3ad)


====================================================================================================================================================================================================================


UNION BASED SQLi nədir ?

UNION operatorundan istifadə etməklə başqa SQL sorğusu yazmağa imkan verən IN BAND (Classic) SQL injection növünə UNION BASED SQLi deyilir.

ERROR BASED (Xəta əsaslı) SQLi nədir ?

ERROR BASED SQL injection SQL verilənlər bazasına aid xəta mesajlarının(əsasən sintaksis) istifadəçilərə göstərilməsi ilə müşahidə olunan IN BAND (Classic) SQL injection növüdür.

BOOLEAN BASED SQLi nədir ?

BOOLEAN BASED SQL injection doğru yanlış sorğular arasında yaranan fərqli cavablar əsasında müəyyən olunan BLİND(İnferential) SQL injection növüdür.

TIME BASED SQLi nədir ?

TIME BASED SQL injection zaman operatorları istifadə etməklə SQL sorğusuna gəlmə zamanı ilə müəyyən olunan BLİND(İnferential) SQL injection növüdür.

OUT-OF-BAND SQLi nədir ?

OUT-OF-BAND SQL injection elə SQLi növüdür ki boşluğu müəyyən etmək üçün eyni kanaldan (nümünə eyni http sorğudan) istifadə edilmir və burada məlumat sorğunun nəticəsi 3 tərəfə göndərilməklə öyrənilir.(Əsasən HTTP,DNS,NTP ... protokollarından istifadə olunur)   

