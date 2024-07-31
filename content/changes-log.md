---
title: "تغییرات نسخه های زبان گو"
type: chapter
weight: 8
---

 ![gopher](../../assets/img/content/changes/logo.png)

 Go هر شش ماه یکبار منتشر می‌شود. هر نسخه‌ی اصلی Go تا زمانی که دو نسخه‌ی اصلی جدیدتر منتشر شوند، پشتیبانی می‌شود. مشکلات بحرانی با انتشار اصلاحات جزئی رفع می‌شوند.

همچنین لینک‌هایی به پروپوزال‌ها (P) و کامیت‌های (C)  ویژگی‌های توضیح داده شده ارائه می‌کنم. برای انگیزه و جزئیات پیاده‌سازی آنها را بررسی کنید.

{{< timeline >}}
	    {{% event date="2024-08-02" title="نسخه 1.23"%}}
- حلقه‌های `for` می‌توانند بر روی توابع تکرارگر (iterator) تکرار کنند.
   - 𝗣 [61405](https://go.dev/issue/61405) 
   - 𝗖𝗟 [557835](https://go.dev/cl/557835), [584596](https://go.dev/cl/584596)
- بسته جدید `iter` با انواع تکرارگر.
   - 𝗣 [61897](https://go.dev/issue/61897) 
   - 𝗖𝗟 [543319](https://go.dev/cl/543319), [557836](https://go.dev/cl/557836), [565935](https://go.dev/cl/565935), [565937](https://go.dev/cl/565937), [591096](https://go.dev/cl/591096)
- تکرارگرهای برش (slice) در بسته `slices`.
   - 𝗣 [61899](https://go.dev/issue/61899) 
   - 𝗖𝗟 [568477](https://go.dev/cl/568477), [595515](https://go.dev/cl/595515)
- تکرارگرهای نقشه (map) در بسته `maps`.
   - 𝗣 [61900](https://go.dev/issue/61900) 
   - 𝗖𝗟 [586716](https://go.dev/cl/586716)
- `Timer`ها و `Ticker`ها که دیگر به وسیله برنامه ارجاع داده نمی‌شوند، بلافاصله برای جمع‌آوری زباله (garbage collection) واجد شرایط می‌شوند.
   - 𝗣 [61542](https://go.dev/issue/61542) 
   - 𝗖𝗟 [512355](https://go.dev/cl/512355)
- از دریافت‌های منسوخ پس از اینکه `Timer`ها و `Ticker`ها `Stop`/`Reset` را برگردانند، اجتناب کنید.
   - 𝗣 [37196](https://go.dev/issue/37196) 
   - 𝗖𝗟 [568341](https://go.dev/cl/568341)
- بسته جدید `unique` امکاناتی برای استانداردسازی مقادیر ارائه می‌دهد.
   - 𝗣 [62483](https://go.dev/issue/62483) 
   - 𝗖𝗟 [574355](https://go.dev/cl/574355)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.23)
    {{% /event %}}
	    {{% event date="2024-02-02" title="نسخه 1.22"%}}
- هر تکرار از حلقه متغیرهای جدیدی ایجاد می‌کند تا از بروز اشکالات به دلیل اشتراک تصادفی جلوگیری کند.
   - 𝗣 [60078](https://go.dev/issue/60078) 
   - 𝗖𝗟 [532580](https://go.dev/cl/532580)
- حلقه‌های `for` می‌توانند بر روی اعداد صحیح تکرار کنند.
   - 𝗣 [61405](https://go.dev/issue/61405) 
   - 𝗖𝗟 [510538](https://go.dev/cl/510538), [538718](https://go.dev/cl/538718)
- بسته جدید `math/rand/v2` برای کار با اعداد تصادفی.
   - 𝗣 [61716](https://go.dev/issue/61716) 
   - 𝗖𝗟 [502495](https://go.dev/cl/502495), [502497](https://go.dev/cl/502497), [502498](https://go.dev/cl/502498), [502499](https://go.dev/cl/502499), [502500](https://go.dev/cl/502500), [502505](https://go.dev/cl/502505), [502506](https://go.dev/cl/502506), [516857](https://go.dev/cl/516857)
- الگوهای مسیریابی HTTP از روش‌ها و wildcards پشتیبانی می‌کنند.
   - 𝗣 [61410](https://go.dev/issue/61410) 
   - 𝗖𝗟 [526815](https://go.dev/cl/526815), [526616](https://go.dev/cl/526616), [528355](https://go.dev/cl/528355), [530575](https://go.dev/cl/530575), [530479](https://go.dev/cl/530479), [530481](https://go.dev/cl/530481), [530461](https://go.dev/cl/530461), [552195](https://go.dev/cl/552195)
- بسته جدید `go/version` برای کار با نسخه‌های Go.
   - 𝗣 [62039](https://go.dev/issue/62039) 
   - 𝗖𝗟 [538895](https://go.dev/cl/538895)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.22)

    {{% /event %}}
	    {{% event date="2023-08-02" title="نسخه 1.21"%}}
- توابع داخلی جدید `min` و `max` کوچک‌ترین/بزرگ‌ترین مقدار را از بین آرگومان‌ها محاسبه می‌کنند.
   - 𝗣 [59488](https://go.dev/issue/59488) 
   - 𝗖𝗟 [496038](https://go.dev/cl/496038), [496257](https://go.dev/cl/496257)
- تابع داخلی جدید `clear` تمام عناصر یک نقشه را حذف یا تمام عناصر یک برش (slice) را صفر می‌کند.
   - 𝗣 [56351](https://go.dev/issue/56351) 
   - 𝗖𝗟 [448076](https://go.dev/cl/448076), [453395](https://go.dev/cl/453395), [463075](https://go.dev/cl/463075), [481935](https://go.dev/cl/481935)
- بسته جدید `log/slog` لاگ‌برداری ساختاریافته با سطوح مختلف را فراهم می‌کند.
   - 𝗣 [56345](https://go.dev/issue/56345) 
   - 𝗖𝗟 [477295](https://go.dev/cl/477295), [484096](https://go.dev/cl/484096), [486376](https://go.dev/cl/486376), [486415](https://go.dev/cl/486415), [487855](https://go.dev/cl/487855), [508195](https://go.dev/cl/508195)
- بسته جدید `slices` عملیات‌های رایج زیادی را بر روی برش‌ها (slices) فراهم می‌کند.
   - 𝗣 [45955](https://go.dev/issue/45955), [54768](https://go.dev/issue/54768), [57348](https://go.dev/issue/57348), [57433](https://go.dev/issue/57433), [58565](https://go.dev/issue/58565), [60091](https://go.dev/issue/60091), [60546](https://go.dev/issue/60546)
   - 𝗖𝗟 [467417](https://go.dev/cl/467417), [468855](https://go.dev/cl/468855), [483175](https://go.dev/cl/483175), [496078](https://go.dev/cl/496078), [498175](https://go.dev/cl/498175), [502955](https://go.dev/cl/502955)
- بسته جدید `maps` چندین عملیات رایج را بر روی نقشه‌ها (maps) فراهم می‌کند.
   - 𝗣 [57436](https://go.dev/issue/57436) 
   - 𝗖𝗟 [464343](https://go.dev/cl/464343)
- بسته جدید `cmp` برای کار با انواع مرتب‌شده (ordered types).
   - 𝗣 [59488](https://go.dev/issue/59488) 
   - 𝗖𝗟 [496356](https://go.dev/cl/496356)
- بهینه‌سازی مبتنی بر پروفایل (PGO) بهینه‌سازی‌ها را بر اساس اطلاعات پروفایل زمان اجرا انجام می‌دهد.
   - 𝗣 [55022](https://go.dev/issue/55022)
- پورت WebAssembly System Interface.
   - 𝗣 [58141](https://go.dev/issue/58141)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.21)
    {{% /event %}}

	    {{% event date="2023-02-02" title="نسخه 1.20"%}}
- تبدیل از یک برش (slice) به یک آرایه (array) مجاز شده است.
   - 𝗣 [46505](https://go.dev/issue/46505) 
   - 𝗖𝗟 [428938](https://go.dev/cl/428938), [430415](https://go.dev/cl/430415), [430475](https://go.dev/cl/430475)
- مقادیر ساختارها (struct) به صورت فیلد به فیلد و به ترتیب تعریف مقایسه می‌شوند.
   - 𝗣 [8606](https://go.dev/issue/8606) 
   - 𝗖𝗟 [237919](https://golang.org/cl/237919), [237921](https://golang.org/cl/237921)
- انواع قابل مقایسه حالا می‌توانند محدودیت‌های `comparable` را برآورده کنند، حتی اگر آرگومان‌های نوع به طور دقیق قابل مقایسه نباشند.
   - 𝗣 [56548](https://go.dev/issue/56548) 
   - 𝗖𝗟 [454575](https://go.dev/cl/454575)
- امکان بسته‌بندی چندین خطا (error) فراهم شده است.
   - 𝗣 [53435](https://go.dev/issue/53435) 
   - 𝗖𝗟 [432898](https://go.dev/cl/432898)
- راهی برای لغو یک `context.Context` با یک خطای خاص ("cause") وجود دارد.
   - 𝗣 [51365](https://go.dev/issue/51365) 
   - 𝗖𝗟 [375977](https://go.dev/cl/375977)
- رشته‌های فرمت `time` جدید برای سازگاری با استانداردهای بین‌المللی.
   - 𝗣 [52746](https://go.dev/issue/52746) 
   - 𝗖𝗟 [412495](https://go.dev/cl/412495)
- بسته جدید `crypto/ecdh` پشتیبانی از پروتکل Elliptic Curve Diffie-Hellman را فراهم می‌کند.
   - 𝗣 [52221](https://go.dev/issue/52221), [56052](https://go.dev/issue/56052) 
   - 𝗖𝗟 [398914](https://go.dev/cl/398914), [450335](https://go.dev/cl/450335)
- دستور `go` اکنون به طور پیش‌فرض `cgo` را در سیستم‌هایی که ابزارهای C ندارند، غیرفعال می‌کند.
   - 𝗖𝗟 [496356](https://go.dev/cl/450739)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.20)
    {{% /event %}}

	    {{% event date="2022-08-02" title="نسخه 1.19"%}}
- مدل حافظه بازنگری شده است.
   - 𝗣 [50859](https://go.dev/issue/50859)
- محدودیت نرم حافظه برای مقدار کل حافظه‌ای که Go استفاده می‌کند.
   - 𝗣 [48409](https://go.dev/issue/48409) 
   - 𝗖𝗟 [397018](https://go.dev/cl/397018)
- محدودیت استفاده کلی CPU توسط GC به 50%، به استثنای زمان بیکاری.
   - 𝗖𝗟 [353989](https://go.dev/cl/353989)
- انواع اتمیک جدید در بسته `sync/atomic`.
   - 𝗣 [50860](https://go.dev/issue/50860) 
   - 𝗖𝗟 [381317](https://go.dev/cl/381317)
- پشتیبانی از لینک‌ها، لیست‌ها، و عناوین واضح‌تر در نظرات مستندات (doc comments).
   - 𝗣 [51082](https://go.dev/issue/51082)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.19)
    {{% /event %}}

	    {{% event date="2022-03-15" title="نسخه 1.18" %}}
- برنامه‌نویسی عمومی با استفاده از پارامترهای نوع.
   - 𝗣 [43651](https://go.dev/issue/43651), [45346](https://go.dev/issue/45346)
- بسته جدید `debug/buildinfo` دسترسی به نسخه‌های ماژول و فلگ‌های ساخت را که در فایل‌های اجرایی جاسازی شده‌اند، فراهم می‌کند.
   - 𝗣 [39301](https://go.dev/issue/39301) 
   - 𝗖𝗟 [353887](https://go.dev/cl/353887)
- بسته جدید `net/netip` نوع آدرس IP بهتر و توابع کمکی را تعریف می‌کند.
   - 𝗣 [46518](https://go.dev/issue/46518) 
   - 𝗖𝗟 [339309](https://go.dev/cl/339309)
- دستور `go get` دیگر بسته‌ها را نمی‌سازد یا نصب نمی‌کند.
   - 𝗣 [43684](https://go.dev/issue/43684)
- آزمون تصادفی (Fuzzing).
   - 𝗣 [44551](https://go.dev/issue/44551)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.18)
    {{% /event %}}

       {{% event date="2021-08-16" title="نسخه 1.17" %}}
- اجازه تبدیل از یک برش (slice) به اشاره‌گر به آرایه (array pointer) داده شده است.
   - 𝗣 [395](https://go.dev/issue/395) 
   - 𝗖𝗟 [216424](https://go.dev/cl/216424)
- بسته `runtime/cgo` تسهیلات متمرکزی برای مدیریت اشیاء اشاره‌گر (c)go فراهم می‌کند.
   - 𝗣 [37033](https://go.dev/issue/37033) 
   - 𝗖𝗟 [295369](https://go.dev/cl/295369)
- محدودیت‌های ساخت مقاوم در برابر اشکال با استفاده از دستور `go:build`.
   - 𝗣 [41184](https://go.dev/issue/41184)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.17)
    {{% /event %}}

       {{% event date="2021-02-16" title="نسخه 1.16" %}}
- جاسازی فایل‌ها در فایل اجرایی با استفاده از دستور `go:embed`.
   - 𝗣 [41191](https://go.dev/issue/41191) 
   - 𝗖𝗟 [243940](https://golang.org/cl/243940), [243941](https://golang.org/cl/243941), [243942](https://golang.org/cl/243942), [243944](https://golang.org/cl/243944), [243945](https://golang.org/cl/243945), [243945](https://golang.org/cl/281492)
- بسته جدید `runtime/metrics` رابط پایداری برای خواندن معیارهای تعریف‌شده توسط پیاده‌سازی از زمان اجرای Go معرفی می‌کند.
   - 𝗣 [37112](https://go.dev/issue/37112) 
   - 𝗖𝗟 [247040](https://golang.org/cl/247040), [247041](https://golang.org/cl/247041), [247043](https://golang.org/cl/247043), [247044](https://golang.org/cl/247044), [247045](https://golang.org/cl/247045), [247046](https://golang.org/cl/247046), [247047](https://golang.org/cl/247047), [247049](https://golang.org/cl/247049)
- بسته جدید `io/fs` رابط‌های سیستم فایل را فراهم می‌کند.
   - 𝗣 [41190](https://go.dev/issue/41190) 
   - 𝗖𝗟 [243908](https://go.dev/cl/243908)
- بسته `io/ioutil` منسوخ شده است.
   - 𝗣 [42026](https://go.dev/issue/42026)
- حالت آگاه به ماژول به طور پیش‌فرض فعال شده است (`GO111MODULE=on`).
   - 𝗣 [41330](https://go.dev/issue/41330)
- دستورهای ساخت مانند `go build` به طور پیش‌فرض `go.mod` و `go.sum` را تغییر نمی‌دهند.
   - 𝗣 [40728](https://go.dev/issue/40728)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.16)
    {{% /event %}}

       {{% event date="2020-08-11" title="نسخه 1.15" %}}
- بسته جدید `time/tzdata` پایگاه داده مناطق زمانی را در برنامه جاسازی می‌کند.
   - 𝗣 [38017](https://go.dev/issue/38017) 
   - 𝗖𝗟 [228101](https://go.dev/cl/228101)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.15)
    {{% /event %}}

       {{% event date="2020-02-25" title="نسخه 1.14" %}}
- اجازه جاسازی رابط‌های همپوشان (overlapping interfaces) داده شده است.
   - 𝗣 [6977](https://go.dev/issue/6977) 
   - 𝗖𝗟 [187519](https://go.dev/cl/187519), [191257](https://go.dev/cl/191257), [214240](https://go.dev/cl/214240), [217134](https://go.dev/cl/217134)
- گوروتین‌ها (goroutines) اکنون به صورت ناهمزمان قابل پیش‌گیری (preemptible) هستند.
   - 𝗣 [24543](https://go.dev/issue/24543) 
   - 𝗖𝗟 [201760](https://go.dev/cl/201760), [201762](https://go.dev/cl/201762)
- بسته جدید `hash/maphash` توابع هش روی دنباله‌های بایت را فراهم می‌کند.
   - 𝗣 [28322](https://go.dev/issue/28322) 
   - 𝗖𝗟 [186877](https://go.dev/cl/186877)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.14)
    {{% /event %}}

       {{% event date="2019-09-03" title="نسخه 1.13" %}}
- مجموعه‌ای یکنواخت و مدرن از پیشوندهای عددی.
   - 𝗣 [19308](https://go.dev/design/19308-number-literals)
- اجازه استفاده از مقادیر صحیح امضا شده به عنوان شمارش جابجایی.
   - 𝗣 [19113](https://go.dev/issue/19113)
- بسته‌بندی خطاها (Error wrapping).
   - 𝗣 [29934](https://go.dev/issue/29934) 
   - 𝗖𝗟 [163558](https://go.dev/cl/163558), [176998](https://go.dev/cl/176998)
- بسته جدید `crypto/ed25519` طرح امضای Ed25519 را پیاده‌سازی می‌کند.
   - 𝗣 [25355](https://go.dev/issue/25355) 
   - 𝗖𝗟 [174945](https://go.dev/cl/174945), [182698](https://go.dev/cl/182698)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.13)
    {{% /event %}}

       {{% event date="2019-02-25" title="نسخه 1.12" %}}
- نقشه‌ها (maps) به ترتیب کلیدها چاپ می‌شوند.
   - 𝗣 [21095](https://go.dev/issue/21095) 
   - 𝗖𝗟 [142737](https://go.dev/cl/142737)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.12)
    {{% /event %}}

       {{% event date="2018-08-24" title="نسخه 1.11" %}}
- ماژول‌ها به عنوان روشی برای مدیریت وابستگی‌ها.
- پورت WebAssembly.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.11)
    {{% /event %}}

       {{% event date="2018-02-16" title="نسخه 1.10" %}}
- `go build` حافظه کشی از بسته‌های اخیراً ساخته‌شده را نگه می‌دارد.
- `go test` نتایج تست را کش می‌کند و به‌طور خودکار `go vet` را اجرا می‌کند.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.10)
    {{% /event %}}

       {{% event date="2017-08-24" title="نسخه 1.9" %}}
- هم‌نام‌سازی نوع‌ها (Type aliases).
   - 𝗣 [18130](https://go.dev/issue/18130)
- ساعت یکنواخت در بسته `time`.
   - 𝗣 [12914](https://go.dev/issue/12914) 
   - 𝗖𝗟 [36255](https://go.dev/cl/36255)
- بسته جدید `math/bits` برای دستکاری بیت‌ها.
   - 𝗣 [18616](https://go.dev/issue/18616) 
   - 𝗖𝗟 [36315](https://go.dev/cl/36315)
- نقشه هم‌زمان (Concurrent map) در بسته `sync`.
   - 𝗣 [18177](https://go.dev/issue/18177) 
   - 𝗖𝗟 [36617](https://go.dev/cl/36617)
- توابع کمکی تست در بسته `testing`.
   - 𝗣 [4899](https://go.dev/issue/4899) 
   - 𝗖𝗟 [38796](https://go.dev/cl/38796)
- کامپایل موازی (Parallel compilation).

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.9)
    {{% /event %}}

       {{% event date="2017-02-16" title="نسخه 1.8" %}}
- نادیده گرفتن برچسب‌ها (tags) هنگام تبدیل یک مقدار از یک نوع ساختار به نوع دیگر.
   - 𝗣 [16085](https://go.dev/issue/16085) 
   - 𝗖𝗟 [30169](https://go.dev/cl/30169), [30190](https://go.dev/cl/30190), [30191](https://go.dev/cl/30191)
- جمع‌آوری زباله (garbage collector) دیگر به‌طور مداوم آرگومان‌ها را در طول کل تابع زنده در نظر نمی‌گیرد.
   - 𝗣 [15843](https://go.dev/issue/15843)
- توابع مربوط به برش‌ها (slice) در بسته `sort`.
   - 𝗣 [16721](https://go.dev/issue/16721) 
   - 𝗖𝗟 [27321](https://go.dev/cl/27321), [30088](https://go.dev/cl/30088)
- ارسال pushهای سرور HTTP/2 در بسته `net/http`.
- خاموشی نرم سرور HTTP در بسته `net/http`.
   - 𝗣 [4674](https://go.dev/issue/4674) 
   - 𝗖𝗟 [32329](https://go.dev/cl/32329)
- پشتیبانی از Context در بسته `database/sql`.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.8)
    {{% /event %}}

       {{% event date="2016-08-15" title="نسخه 1.7" %}}
- بسته جدید `context` برای کار با مهلت‌ها و لغو.
   - 𝗣 [14660](https://go.dev/issue/14660) 
   - 𝗖𝗟 [20346](https://go.dev/cl/20346), [20347](https://go.dev/cl/20347)
- بسته جدید `net/http/httptrace` برای ردیابی رویدادها در درخواست‌های HTTP.
   - 𝗣 [12580](https://go.dev/issue/12580) 
   - 𝗖𝗟 [22191](https://go.dev/cl/22191)
- زیر-تست‌ها و زیر-بنچمارک‌ها در بسته `testing`.
   - 𝗖𝗟 [18895](https://go.dev/cl/18895), [18896](https://go.dev/cl/18896)

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.7)
    {{% /event %}}


    {{% event date="2016-02-17" title="نسخه 1.6" %}}
- پشتیبانی از HTTP/2 در بسته `net/http`.
- Vendoring.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.6)
    {{% /event %}}


    {{% event date="2015-08-19" title="نسخه 1.5" %}}
- کامپایلر و زمان اجرا به‌طور کامل در Go نوشته شده‌اند.
- جمع‌آوری زباله (garbage collection) هم‌زمان.
- به‌طور پیش‌فرض، `GOMAXPROCS` به تعداد هسته‌های در دسترس تنظیم می‌شود.
- بسته‌های داخلی.
- دستور `go tool trace` برای ردیابی دقیق اجرای برنامه.
- دستور `go doc` برای ساخت مستندات بسته.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.5)
    {{% /event %}}

       {{% event date="2014-12-10" title="نسخه 1.4" %}}
- حلقه for-range بدون متغیرها.
- عدم اجازه فراخوانی متدها بر روی `**T`.
- دستور `go generate` برای تولید کد منبع قبل از کامپایل.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.4)
    {{% /event %}}

       {{% event date="2014-06-18" title="نسخه 1.3" %}}
- استک‌های هم‌پیوسته goroutine.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.3)
    {{% /event %}}

       {{% event date="2013-12-01" title="نسخه 1.2" %}}
- هر بیانیه‌ای که صراحتاً یا ضمنی نیاز به ارزیابی یک آدرس `nil` داشته باشد، خطا است.
- بیان کامل برش برای مشخص کردن ظرفیت و طول هنگام برش.
- بسته جدید `encoding` مجموعه‌ای از رابط‌های کدگذاری استاندارد برای ساخت marshalers و unmarshalers سفارشی را فراهم می‌کند.
- بسته جدید `image/color/palette` پالت‌های رنگی استاندارد را ارائه می‌دهد.
- عملیات ایندکسینگ در مشخصات قالب‌بندی `fmt`.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.2)
    {{% /event %}}

       {{% event date="2013-05-13" title="نسخه 1.1" %}}
- تقسیم عدد صحیح بر صفر یک خطای زمان کامپایل است.
- مقادیر متد.
- شناسایی خطاهای هم‌زمان (Race detector).
- بسته جدید `go/format` روشی برای دسترسی به قابلیت‌های قالب‌بندی دستور `go fmt` ارائه می‌دهد.
- بسته جدید `net/http/cookiejar` اصول مدیریت کوکی‌های HTTP را فراهم می‌کند.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1.1
    {{% /event %}}

       {{% event date="2012-03-28" title="نسخه 1" %}}
- اولین نسخه پایدار.

[یادداشت‌های نسخه](https://tip.golang.org/doc/go1)
    {{% /event %}}

{{< /timeline >}}
