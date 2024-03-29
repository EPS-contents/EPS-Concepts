امید ریاضی
========================
قبل از آنکه دقیق بگوییم امید ریاضی چیست و چگونه محاسبه می شود بگذارید درمورد میانگین کمی صحبت کنیم.
همانطور که به یاد دارید میانگین جامعه را با رابطه زیر تعریف میکردیم.
$$ \overline{x}= \frac{1}{n}  \sum_{i=1}^n x_{i} $$
فرض کنید پیشامد های محتمل را با $$x_{i}$$ نمایش دهیم و تعداد پیش آمدن هر رخداد را $$n_{i}$$ بنامیم آنگاه رابطه بالا بصورت زیر قابل بازنویسی است
$$ \overline{x}= \frac{1}{n}  \sum_{all x_{i}} n_{i}x_{i} = \sum_{all x_{i}} \frac{n_{i}}{n}x_{i} $$
خب همانطور که میدانیم $$\frac{n_{i}}{n}$$ فراوانی نسبی است و به عبارتی تقریب احتمال است. زمانی که تعداد آزمایشات زیاد شود مقدار $$\frac{n_{i}}{n}$$ به احتمال یا همان $$P(x)$$ نزدیک می شود.
پس خواهیم داشت:
 $$\sum_{all x_{i}} P(x_i)x_{i} $$
 رابطه بالا را به عنوان تعریف ریاضی امید ریاضی تعریف می شود.  
     
```{admonition} نکته!
:class: note
امید ریاضی را مقدار مورد انتظار نیز میگویند و از رابطه زیر تعریف می شود:
$$E[X]=\sum_{all x_{i}} P(x_i)x_{i}$$
```

```{admonition} مثال
:class: tip
پوریا و علی در حال دیدن آگهی های بازرگانی بودند که آگهی یک مسابقه میلیونی را مشاهده کردند محتوای آگهی بدین صورت بود:
با ارسال عدد 1 به سامانه پیامکی ما، برنده خوش شانس یک جایزه 10 میلیون تومانی باشید!
علی که علاقه مند به مسابقه بود به پوریا پیشنهاد شرکت کردن در این مسابقه را داد پوریا اما قبل از اینکه به علی پاسخ دهد از دانش احتمال خود استفاده کرد و با خود گفت که هزینه ارسال پیامک 1000 تومان است و طبق آمار قبلی میدانم حدود 20 میلیون نفر در مسابقه شرکت خواهند کرد.
او متغییر $$X$$ را برابر مقدار موجودی حسابش بعد از قرعه کشی قرار داد و محاسبات را شروع کرد:
پوریا با خود گفت احتمال برنده شدن من در این جمعیت برابر بااحتمال زیر خواهد بود:
$$P(x) =\begin{cases}win & P(x) = \frac{1}{20000000}\\lose & P(x) = \frac{19999999}{20000000}\end{cases}$$
پس از آن گفت اگر این جایزه را برنده شوم موجودی حسابم می شود مقدار جایزه منهای هزینه ورودی.
پس خواهیم داشت:
$$x =\begin{cases}win & x = +10,000,000-1,000=+9,999,000\\lose & x =- 1,000\end{cases}$$
و با توجه به رابطه امید ریاضی خواهیم داشت:
$$E[X]=\sum_{all x_{i}} P(x_i)x_{i}=\frac{1}{20000000}\times (+9,999,000)+\frac{19999999}{20000000}\times (-1,000)=-999.5$$
طبق محاسبات متوجه شد مقدار پول مورد انتظارش بعد از قرعه کشی منفی 999.5 تومان خواهد بود و ضرر خواهد کرد.
پس از محاسبات متوجه شد ورود به این مسابقه به نفعش نیست!
```
### خواص امید ریاضی
```{admonition}مثال
:class: note
اگر $$X$$ و $$Y$$ متغییر تصادفی باشند، آنگاه:
* $$E[aX+b]=aE[X]+b$$
* $$E[X+Y]=E[y]+E[X]$$
* $$E[g(X)]=\sum_{x} g(x) f_{X}(x)$$
```
### LOTUS
فرض کنید که:
$$Y=g(X)$$
$$E[Y]=\sum_{y}  y f_{y}(y)$$
$$E[g(X)]=\sum_{y}  y P(g(X)=y)=\sum_{y}  y P(x=g^{-1}(y))=\sum_{y}  y\sum_{x=g^{-1}(y)}  f_{X}(x)=\sum_{y} \sum_{x=g^{-1}(y)}yf_{X}(x) $$
$$\Rightarrow E[g(X)]=\sum_{x} g(x) f_{X}(x)$$  
به نوعی می توان اینگونه بیان کرد اگر ما متغیر X را داشته باشیم و تابعی بر اساس آن شکل بگیرد که ما اینجا $$Y=g(X)$$ در نظر گرفتیم، در صورتی که یک به یک نباشد مثلا $$g(X)=X^2$$
و اگر فرض کنیم $$X={-1,1,3}$$ که احتمال رخ دادن هر کدامشان $$ \frac{1}{3} $$  باشد آنگاه خواهیم داشت $$Y={1,9}$$  و دیگر احتمال این رخ دادن این دو با یکدیگر برابر نیست احتمال رخ دادن 1 $$ \frac{2}{3} $$  و احتمال رخ دادن 9 $$ \frac{1}{3} $$ است.  
به زبان ساده این رابطه نیز همین را می گویید، میگویید برای X هایی که خروجی هایشان بعد از ورود به تابع $$Y=g(X)$$ یکسان است، باید ابتدا احتمال رخ دادن آن X ها را با یکدیگر جمع کنیم سپس در مقدار خروجی تابع ضرب کنیم :)  
برای توابع یک به یک درک این فرمول راحت تر است.
### منابع 
* The cartoon guide to statistics,Larry Gonic and Woollcott Smith
* [مکتب خونه](https://maktabkhooneh.org/course/%D8%A2%D9%85%D8%A7%D8%B1-%D8%A7%D8%AD%D8%AA%D9%85%D8%A7%D9%84-%D9%85%D9%87%D9%86%D8%AF%D8%B3%DB%8C-mk627/%D9%81%D8%B5%D9%84-%D8%A7%D9%88%D9%84-%D8%A2%D9%85%D8%A7%D8%B1-%D8%A7%D8%AD%D8%AA%D9%85%D8%A7%D9%84-%D9%85%D9%87%D9%86%D8%AF%D8%B3%DB%8C-ch1733/%D9%88%DB%8C%D8%AF%DB%8C%D9%88-%D8%AA%D8%A7%D8%A8%D8%B9-%D8%AC%D8%B1%D9%85-%D8%A7%D8%AD%D8%AA%D9%85%D8%A7%D9%84-%D8%AA%D9%88%D8%B2%DB%8C%D8%B9-%D8%AA%D8%AC%D9%85%DB%8C%D8%B9%DB%8C-%D8%A7%D8%AD%D8%AA%D9%85%D8%A7%D9%84-%D8%A7%D9%85%DB%8C%D8%AF/) 
* https://en.wikipedia.org/wiki/Law_of_the_unconscious_statistician#CITEREFFederer1969 
* [مکتب خونه](https://maktabkhooneh.org/course/%D8%A2%D9%85%D8%A7%D8%B1-%D8%A7%D8%AD%D8%AA%D9%85%D8%A7%D9%84-%D9%85%D9%87%D9%86%D8%AF%D8%B3%DB%8C-mk627/%D9%81%D8%B5%D9%84-%D8%A7%D9%88%D9%84-%D8%A2%D9%85%D8%A7%D8%B1-%D8%A7%D8%AD%D8%AA%D9%85%D8%A7%D9%84-%D9%85%D9%87%D9%86%D8%AF%D8%B3%DB%8C-ch1733/%D9%88%DB%8C%D8%AF%DB%8C%D9%88-conditional-joint-distribution-lotus/) 
