---
title: Hata ayıklayıcıya ilk bakış
description: Visual Studio hata ayıklayıcısını kullanarak uygulamaları hata ayıklamaya başlama
ms.custom: seoapril2019
ms.date: 04/08/2019
ms.topic: quickstart
helpviewer_keywords:
- debugger
ms.assetid: c763d706-3213-494f-b4d2-990b6e1ec456
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 249b8aa88b11643ed0b353df25bef3a054ef5e55
ms.sourcegitcommit: 0e482cfc15f809b564c3de61646f29ecd7bfcba6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/14/2019
ms.locfileid: "70987784"
---
# <a name="first-look-at-the-visual-studio-debugger"></a>Visual Studio hata ayıklayıcısına ilk bakış

Bu konuda, Visual Studio tarafından sunulan hata ayıklayıcı araçları tanıtılmaktadır. Visual Studio bağlamında, uygulamanızda *hata ayıklarken*, genellikle uygulamayı hata ayıklayıcı ekli olarak (hata ayıklayıcı modunda) çalıştırdığınız anlamına gelir. Bunu yaptığınızda, hata ayıklayıcı, kodunuzun ne yaptığını görmek için birçok yol sağlar. çalışırken. Kodunuzda saklanan değerlere bakabilir ve değişkenlerde depolanan değerlere bakabilirsiniz, değerlerin ne zaman değişiklik olduğunu görmek için, değişkenlerinizin yürütme yolunu inceleyebilirsiniz. Kodu ilk kez ayıklamaya çalıştığınızda, bu konuya geçmeden önce [mutlak yeni başlayanlar Için hata ayıklama](../debugger/debugging-absolute-beginners.md) işlemini okumak isteyebilirsiniz.

Burada açıklanan özellikler, Visual Studio tarafından C#desteklenen C++,, Visual Basic, JavaScript ve diğer diller için geçerlidir (aksi belirtilmedikçe).

## <a name="set-a-breakpoint-and-start-the-debugger"></a>Bir kesme noktası ayarlayın ve hata ayıklayıcıyı başlatın

Hata ayıklamak için, uygulama işlemine eklenmiş hata ayıklayıcı ile uygulamanızı başlatmanız gerekir. **F5** (Hata ayıklama **> Başlat**) bunu yapmanın en yaygın yoludur. Ancak, artık uygulama kodunuzu incelemek için herhangi bir kesme noktası ayarlanmamış olabilirsiniz; bu nedenle, önce bunu yapacağız ve ardından hata ayıklamayı başlatacak. Kesme noktaları güvenilir hata ayıklama en temel hem de temel özelliğidir. Bir kesme noktası değişkenlerin değerleri veya bellek davranışını göz olabilmesi için Visual Studio çalışan kodunuzu nereye askıya almanız ya da bir dal kod getting run olup olmadığını gösterir.

Kod Düzenleyicisi 'nde açık bir dosyanız varsa, bir kod satırının solundaki kenar boşluğuna tıklayarak bir kesme noktası ayarlayabilirsiniz.

![Kesme noktası ayarlama](../debugger/media/dbg-tour-set-a-breakpoint.gif "Kesme noktası ayarlama")

**F5** tuşuna basın (hata ayıklama **> başlatın**) veya **hata ayıklamayı Başlat** düğmesine başla(../debugger/media/dbg-tour-start-debugging.png "hata ayıklama araç") çubuğunda ![hata ayıklamayı Başlat]ve hata ayıklayıcı, karşılaştığı ilk kesme noktasında çalışır. Uygulama henüz çalışmıyorsa, F5 hata ayıklayıcıyı başlatır ve ilk kesme noktasında durmaktadır.

Kod satırının veya ayrıntılı olarak incelemek istediğiniz kod bölümünün bildiğiniz durumlarda kesme noktaları yararlı bir özelliktir.

## <a name="navigate"></a>Adım komutlarını kullanarak hata ayıklayıcıda kodda gezinin

Çoğu komut için klavye kısayolları sağlıyoruz, çünkü uygulama kodunuzun daha hızlı bir şekilde gezinmesine dikkat edin. (Menü komutları gibi eşdeğer komutlar parantez içinde gösterilir.)

Uygulamanızı hata ayıklayıcı eklenmiş olarak başlatmak için, **F11** tuşuna basın (**hata ayıklama > adımla**). F11 olan **içine adımla** komut ve aynı anda uygulama yürütme bir deyim ilerler. Uygulamayı F11 ile başlattığınızda, hata ayıklayıcı yürütülen ilk deyimde kesilir.

![F11 step INTO](../debugger/media/dbg-tour-f11.png "F11 step INTO")

Sarı ok, aynı zamanda aynı noktayı (Bu bildirimi henüz çalıştırılmadı) uygulama yürütmeyi askıya alır, hata ayıklayıcı durduruldu, deyimi temsil eder.

F11 çoğu ayrıntılı yürütme akışı incelemek için iyi bir yoludur. (Kod üzerinden daha hızlı hareket etmek için diğer bazı seçenekleri de göstereceğiz.) Varsayılan olarak, kullanıcı dışı kod üzerinde hata ayıklayıcı atlar (daha ayrıntılı bilgi isterseniz bkz [yalnızca kendi kodum](../debugger/just-my-code.md)).

>[!NOTE]
> Yönetilen kodda, özellikleri ve işleçleri (varsayılan davranış) üzerinde otomatik olarak adımla uyarılmak isteyip istemediğinizi soran bir iletişim kutusu görürsünüz. Ayarı daha sonra değiştirmek istiyorsanız, **hata ayıklama**altındaki **Araçlar > Seçenekler** menüsünde **Özellikler ve işleçler üzerinde adımla** ayarını devre dışı bırakın.

## <a name="step-over-code-to-skip-functions"></a>İşlevleri atlamak için kodun üzerinde adımla

Bir işlev veya yöntem çağrısı olan bir kod satırından olduğunuzda, **F11 (** **Hata Ayıkla > Step Over**) tuşuna basarak F11 yerine + tuşlarına basabilirsiniz.

F10 uygulama kodunuzda işlevlere veya yöntemlere adımla hata ayıklayıcıyı ilerletir (kod yine de çalıştırılır). F10 tuşuna basarak, ilgilenmediğiniz kodu atlayabilirsiniz. Bu şekilde, daha fazla ilgilendiğiniz koda hızlı bir şekilde ulaşabilirsiniz.

## <a name="step-into-a-property"></a>Bir özelliğe adımla

Daha önce belirtildiği gibi, hata ayıklayıcı yönetilen özellikleri ve alanları atlar, ancak **belirli komuta adım** bu davranışı geçersiz kılmanıza olanak tanır.

Bir özellik veya alana sağ tıklayın ve **belirli bir adımla**' i seçin, sonra da kullanılabilir seçeneklerden birini belirleyin.

![Belirli bir adımla](../debugger/media/dbg-tour-step-into-specific.png "Belirli bir adımla")

Bu örnekte, **belirli bir adımla** ilgili `Path.set`kodu bize alır.

![Belirli bir adımla](../debugger/media/dbg-tour-step-into-specific-2.png "Belirli bir adımla")

## <a name="run-to-a-point-in-your-code-quickly-using-the-mouse"></a>Fareyi kullanarak kodunuzda bir noktaya hızla çalışma

Hata ayıklayıcıda, sol tarafta çalıştırılacak **şekilde** Çalıştır (yürütmeyi buraya kadar Çalıştır ![) düğmesine tıklayarak](../debugger/media/dbg-tour-run-to-click.png "") bir kod satırının üzerine gelin.

![Tıklanan satıra kadar Çalıştır](../debugger/media/dbg-tour-run-to-click-2.png "tıklanan satıra kadar Çalıştır")

> [!NOTE]
> **Tıklama Için Çalıştır** (yürütmeyi buraya kadar Çalıştır) düğmesi, ' den itibaren [!include[vs_dev15](../misc/includes/vs_dev15_md.md)]kullanılabilir.

**Çalıştırmak Için Çalıştır** ' a tıklayın (yürütmeyi buraya kadar Çalıştır) düğmesine tıklayın. Hata ayıklayıcı, tıklattığınız kod satırına ilerler.

Bu düğmeyi kullanarak geçici bir kesme noktası ayarlayarak benzer. Bu komut, uygulama kodunun görünür bir bölgesinde hızlıca elde etmek için de kullanışlıdır. **Çalıştır ' ı** kullanarak herhangi bir açık dosyayı tıklatabilirsiniz.

## <a name="advance-the-debugger-out-of-the-current-function"></a>Hata ayıklayıcıyı geçerli işlevin dışına ilerletin

Bazen hata ayıklama oturumunuzu devam ettirmek, ancak hata ayıklayıcıyı geçerli işlev aracılığıyla ilerletmek isteyebilirsiniz.

**SHIFT + F11** tuşlarına basın (veya **hata ayıklama > Step Out**).

Bu komut, uygulama yürütmeyi devam ettirir (ve hata ayıklayıcı ilerler) geçerli işlev dönene kadar.

## <a name="run-to-cursor"></a>İmlece kadar Çalıştır

Hata **ayıklamayı Durdur Red düğmesine** basarak(../debugger/media/dbg-tour-stop-debugging.png "hata ayıklamayı Durdur") hata ![ayıklamayı Durdur]veya **SHIFT** + **F5**.

Uygulamanızdaki bir kod satırına sağ tıklayın ve **Imlece Çalıştır**' ı seçin. Bu komut, hata ayıklamaya başlar ve geçerli kod satırında geçici bir kesme noktası ayarlar.

![Imlece kadar Çalıştır](../debugger/media/dbg-tour-run-to-cursor.png "Imlece kadar Çalıştır")

Kesme noktaları ayarladıysanız, hata ayıklayıcı, isabet eden ilk kesme noktasında duraklatılır.

**Imlece çalıştırmayı**seçtiğiniz kod satırına ulaşana kadar **F5** tuşuna basın.

Bu komut, kodu düzenlediğinizde ve hızlı bir şekilde geçici bir kesme noktası ayarlamak ve hata ayıklayıcıyı aynı anda başlatmak istediğinizde yararlıdır.

> [!NOTE]
> Hata ayıklarken **çağrı yığını** penceresinde **imlece imlecini** kullanabilirsiniz.

## <a name="restart-your-app-quickly"></a>Uygulamanızı hızlı bir şekilde yeniden başlatın

Hata ayıklama araç çubuğundaki uygulamayı **Yeniden Başlat** ![uygulamayı](../debugger/media/dbg-tour-restart.png "Yeniden Başlat düğmesine tıklayın") (**Ctrl + Shift + F5**).

Bastığınızda **yeniden**, uygulama durdurup hata ayıklayıcı yerine zaman kaydeder. İlk kesme noktasına isabet kodu yürüterek, hata ayıklayıcı duraklatır.

(../debugger/media/dbg-tour-stop-debugging.png "Hata ayıklayıcıyı") durdurmak ve kod düzenleyicisine geri dönmek Istiyorsanız, **yeniden başlatma**yerine ![Red Durdur hata ayıklamayı Durdur düğmesine]basabilirsiniz.

## <a name="edit-your-code-and-continue-debugging-c-vb-c-xaml"></a>Kodunuzu düzenleyin ve hata ayıklamaya devam edinC#(, vb C++, XAML)

Visual Studio tarafından desteklenen çoğu dillerde hata ayıklama oturumu ortasında kodunuzu düzenleyin ve hata ayıklamaya devam et. Bu özelliği kullanmak için imlecinizi hata ayıklayıcı, düzenlemeleri yapma ve ENTER tuşuna duraklatıldığı sırada kodunuzu tıklayın **F5**, **F10**, veya **F11** hata ayıklamaya devam etmek için.

![Düzenle ve devam et hata ayıklama](../debugger/media/dbg-tips-edit-and-continue.gif "EditAndContinue")

Özelliğini kullanarak ve özellik kısıtlamaları hakkında daha fazla bilgi için bkz. [Düzenle ve devam et](../debugger/edit-and-continue.md).

Bir hata ayıklama oturumu sırasında XAML kodunu değiştirmek için bkz. xaml [üzerinde çalışan xaml kodunu yazma ve hata ayıklama xaml çalışırken yeniden yükleme](xaml-hot-reload.md).

## <a name="inspect-variables-with-data-tips"></a>Veri ipuçları değişkenlerle inceleyin

Biraz kısa bir süre içinde sizi öğrenmiş olduğunuza göre, uygulama durumunu (değişkenler) hata ayıklayıcıyla araştırmanız için iyi bir fırsattır. Değişkenleri incelemenizi sağlayan özellikler, hata ayıklayıcının en faydalı özelliklerinden bazılarıdır ve bunu yapmak için farklı yollar vardır. Genellikle, bir sorunu ayıklamaya çalıştığınızda, değişkenlerin belirli bir uygulama durumunda olmasını istediğiniz değerleri depolayıp depoladığını bulmaya çalışıyorsunuz.

Hata ayıklayıcıda duraklalarken, fareyle bir nesnenin üzerine gelin ve varsayılan özellik değerini görürsünüz (Bu örnekte, dosya adı `market 031.jpg` varsayılan özellik değeridir).

![Veri Ipucunu görüntüleme](../debugger/media/dbg-tour-data-tips.gif "Veri Ipucunu görüntüleme")

Tüm özelliklerini görmek için nesneyi genişletin (Bu örnekteki `FullPath` özelliği gibi).

Genellikle, hata ayıklama sırasında istediğiniz nesnelerin özellik değerlerini denetlemek için hızlı bir yol ve veri ipuçları yapmak için iyi bir yoludur.

> [!TIP]
> Desteklenen çoğu dilde kodu bir hata ayıklama oturumunun ortasında düzenleyebilirsiniz. Daha fazla bilgi için bkz. [Düzenle ve devam et](../debugger/edit-and-continue.md).

## <a name="inspect-variables-with-the-autos-and-locals-windows"></a>Otolar ve yerel öğeler pencerelerinde değişkenlerle inceleyin

Hata ayıklarken, kod düzenleyicisinin alt kısmındaki **oto** penceresine bakın.

![Oto penceresi](../debugger/media/dbg-tour-autos-window.png "Oto penceresi")

**Oto** penceresinde, değişkenleri geçerli değerleri ve türleri ile birlikte görürsünüz. **Oto** penceresi, geçerli satırda veya önceki satırda kullanılan tüm değişkenleri gösterir (içinde C++, pencerede önceki üç kod satırındaki değişkenler gösterilir. Dile özgü davranışın belgelerini denetleyin).

> [!NOTE]
> JavaScript 'te, **Yereller** penceresi desteklenir, ancak **oto** penceresi desteklenmez.

Sonra, **Yereller** penceresine bakın. **Yereller** penceresi, şu anda kapsamda olan değişkenleri gösterir.

![Yereller penceresi](../debugger/media/dbg-tour-locals-window.png "Yereller penceresi")

Bu örnekte, `this` nesnesi ve nesnesi `f` kapsamdadır. Daha fazla bilgi için bkz. [oto ve Yereller pencerelerinde değişkenleri İnceleme](../debugger/autos-and-locals-windows.md).

## <a name="set-a-watch"></a>Bir izleme ayarlayın

Kullanabileceğiniz bir **Watch** penceresinin bir değişken (veya bir ifade) takip etmek istediğinizi belirtin.

Hata ayıklarken, bir nesneye sağ tıklayın ve **Gözcü Ekle**' yi seçin.

![Gözcü penceresi](../debugger/media/dbg-tour-watch-window.png "İzleme penceresi")

Bu örnekte, `f` nesnesinde bir izleme kümesi vardır ve hata ayıklayıcıda geçiş yaparken değer değişikliğini görebilirsiniz. Diğer değişken pencerelerinin aksine, **Watch** Windows her zaman izlemekte olduğunuz değişkenleri gösterir (kapsam dışında gri renkte bulunur).

Daha fazla bilgi için bkz [. gözcü ve hızlı gözcü pencerelerini kullanarak Izleme ayarlama](../debugger/watch-and-quickwatch-windows.md)

## <a name="examine-the-call-stack"></a>Çağrı yığınını inceleyin

Hata ayıklarken **çağrı yığını** penceresine, varsayılan olarak sağ alt bölmede da açık ' a tıklayın.

![Çağrı yığınını inceleyin](../debugger/media/dbg-tour-call-stack.png "Çağrı yığınını inceleyin")

**Çağrı yığını** penceresi, yöntemleri ve işlevleri çağrılır sırasını gösterir. Geçerli işlev en üst satırına gösterir ( `Update` Bu örnekte yöntemi). İkinci satır, `Path.set` özelliğinden çağrılan `Update` ve bu şekilde devam eden gösterir. Çağrı yığınını inceleyebilir ve bir uygulamanın yürütme akışını anlamanıza için iyi bir yoludur.

> [!NOTE]
> **Çağrı yığını** penceresi benzer hata ayıklama perspektifi için Eclipse gibi bazı IDE içinde.

Bir satır kod, kaynak koda bakmaktır gitmek için çift tıklayın ve hata ayıklayıcı tarafından denetlenmekte olan geçerli kapsamını da değişiklikler. Bu, hata ayıklayıcıyı ilerlemez.

Sağ tıklama menülerden kullanabilirsiniz **çağrı yığını** başka şeyler için pencere. Örneğin, belirli işlevlere kesme noktaları ekleyebilirsiniz, uygulamayı **Imlece Çalıştır**' ı kullanarak yeniden başlatabilir ve kaynak kodunu inceleyebilirsiniz. Bkz [. nasıl yapılır: Çağrı yığınını](../debugger/how-to-use-the-call-stack-window.md)inceleyin.

## <a name="exception"></a>Özel durumu inceleyin

Uygulamanız bir özel durum oluşturduğunda, hata ayıklayıcı sizi özel durumu oluşturan kod satırına götürür.

![Özel durum Yardımcısı](../debugger/media/dbg-tour-exception-helper.png "Özel durum Yardımcısı")

Bu örnekte, **özel durum Yardımcısı** size bir `System.Argument` özel durum ve yolun geçerli bir form olmadığını belirten bir hata iletisi gösterir. Bu nedenle, bir yöntem veya işlev bağımsız değişkeninde oluşan hatayı biliyoruz.

Bu örnekte, `DirectoryInfo` çağrı, `value` değişkende depolanan boş dizede hata verdi.

Özel durum Yardımcısı, hata ayıklamanıza yardımcı olabilecek harika bir özelliktir. Hata ayrıntılarını görüntüle ve özel durum Yardımcısı 'ndan bir izleme ekleme gibi işlemler de yapabilirsiniz. Ya da gerekirse, belirli bir özel durumu oluşturma koşullarını değiştirebilirsiniz. Kodunuzda özel durumların nasıl işleneceği hakkında daha fazla bilgi için bkz. [hata ayıklama teknikleri ve araçları](../debugger/write-better-code-with-visual-studio.md).

> [!NOTE]
> Özel durum Yardımcısı, ' [!include[vs_dev15](../misc/includes/vs_dev15_md.md)]den Itibaren özel durum yardımcısını değiştirdi.

Bu özel durum türünün nasıl işleneceği hakkında daha fazla seçenek görmek için **özel durum ayarları** düğümünü genişletin, ancak bu tur için herhangi bir şeyi değiştirmeniz gerekmez!

## <a name="debug-live-aspnet-apps-in-azure-app-service"></a>Azure App Service 'da canlı ASP.NET uygulamalarında hata ayıklama

**Snapshot Debugger** , yürütirken ilgilendiğiniz kodun yürütüldüğü üretim içi uygulamalarınızın anlık görüntüsünü alır. Bir anlık görüntüsünü almak için hata ayıklayıcı açmasını sağlamak için anlık görüntü noktaları ve günlüğe kaydetme noktaları kodunuzda ayarlayın. Hata ayıklayıcı, tam olarak üretim uygulamanızın trafiğini etkilemeden, çıktığına görmenizi sağlar. Snapshot Debugger, üretim ortamlarında ortaya çıkan sorunları çözmek için gereken süreyi ciddi ölçüde azaltmaya yardımcı olabilir.

![Snapshot Debugger 'ı başlatın](../debugger/media/snapshot-launch.png "Snapshot Debugger 'ı başlatın")

Anlık görüntü koleksiyonu, Azure App Service çalıştıran ASP.NET uygulamaları için kullanılabilir. ASP.NET uygulamaları .NET Framework 4.6.1 veya üzeri sürümlerde çalışıyor olmalıdır ve ASP.NET Core uygulamalar Windows üzerinde .NET Core 2,0 veya sonraki sürümlerde çalışıyor olmalıdır.

Daha fazla bilgi için bkz. [Snapshot Debugger kullanarak canlı ASP.NET uygulamalarında hata ayıklama](../debugger/debug-live-azure-applications.md).

## <a name="view-snapshots-with-intellitrace-step-back-visual-studio-enterprise"></a>IntelliTrace adım geri (Visual Studio Enterprise) ile anlık görüntüleri görüntüleme

**IntelliTrace adım geri** alma, her kesme noktası ve hata ayıklayıcı adım olayında uygulamanızın bir anlık görüntüsünü otomatik olarak alır. Kaydedilen anlık görüntü, önceki kesme noktaları veya adımlara geri dönün ve daha önce olduğu gibi uygulama durumunu görüntülemek etkinleştirin. IntelliTrace geri adım atma önceki uygulama durumu görmek istiyorsanız ancak hata ayıklamayı yeniden başlatın veya istenen uygulama durumu yeniden istemediğiniz durumlarda size zaman kazandırabilir.

Hata ayıklama araç çubuğundaki **geri** ve **adım ileri** düğmelerini kullanarak anlık görüntülerle gezinerek görüntüleyebilirsiniz. Bu düğmeler **Tanılama araçları** penceresindeki **Olaylar** sekmesinde görüntülenen olaylara gider.

![Geri adımla ve Ilet düğmeleri](../debugger/media/intellitrace-step-back-icons-description.png  "Geri adımla ve ilet düğmeleri")

Daha fazla bilgi için bkz. [IntelliTrace kullanarak önceki uygulama durumlarını İnceleme](../debugger/view-historical-application-state.md) sayfası.

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticide birçok hata ayıklayıcı özelliğine hızlı bir bakış sunuyoruz. Kesme noktaları gibi bu özelliklerden birine daha ayrıntılı bir bakış istemeniz gerekebilir.

> [!div class="nextstepaction"]
> [Kesme noktaları kullanmayı öğrenin](../debugger/using-breakpoints.md)
