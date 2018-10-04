---
title: Hata ayıklayıcısında simge (.pdb) ve kaynak dosyaları belirtme | Microsoft Docs
ms.custom: H1Hack27Feb2017
ms.date: 04/05/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- VS.ToolsOptionsPages.Debugger.Native
- VS.ToolsOptionsPages.Debugger.Symbols
- vs.debug.options.Native
- vs.debug.nosymbols
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- source code
- .dbg files
- source code, managing
- symbols, managing
- .pdb files
- dbg files
- pdb files
- debugger
ms.assetid: 1105e169-5272-4e7c-b3e7-cda1b7798a6b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1b50bdf48e80e5ed259ba61f0e104e411e76a490
ms.sourcegitcommit: b2942b8aa93bf73747790a05b67908c0b0108afe
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48788038"
---
# <a name="specify-symbol-pdb-and-source-files-in-the-visual-studio-debugger"></a>Visual Studio hata ayıklayıcısında simge (.pdb) ve kaynak dosyaları belirtme
Ayrıca bir sembol dosyası olarak da bilinen program veritabanı (.pdb) dosyası, kaynak kodu sınıfları, yöntemleri ve diğer tanımlayıcıları projenizin derlenen yürütülebilir kullanılan kodu için içinde oluşturduğunuz eşleştirir. .Pdb dosyası, kaynak kodundaki deyimleri yürütülebilir dosyalardaki yürütme yönergeleriyle de eşleştirir. Hata ayıklayıcı iki temel bilgi parçasını belirlemek için bu bilgileri kullanır:

* Visual Studio IDE içinde görüntülenecek kaynak dosya ve satır numarası adı
* Bir kesme noktası ayarlarsanız durdurulacak yürütülebilir öğenin konumu

Sembol dosyası ayrıca orijinal kaynak dosyası konumunu ve isteğe bağlı olarak, kaynak dosyasının alındığı kaynak sunucusunun konumunu içerir.
  
> [!TIP]
> Proje kaynak kodunuz dışında kod hatası ayıklamak istiyorsanız, Windows kod veya üçüncü taraf kodu gibi proje çağrılarınızda, konumunu .pdb (ve isteğe bağlı olarak, harici kod kaynak dosyalarını) belirtmeniz gerekir ve bu dosyaları t derleme tam olarak eşleşmesi gerekir He yürütülebilir. 

##  <a name="how-can-i-manage-symbol-files-while-debugging"></a>Sembol dosyaları ayıklarken nasıl yönetebilirim? 

**Modülleri** penceresi, hata ayıklayıcı değerlendirmesini kullanıcı kodu veya My Code ve yükleme durumu modülü için sembol olarak hangi kod modülleri öğrenebilirsiniz. Ayrıca bu pencereyi hata ayıklama sırasında sembolleri yüklemek üzere de kullanabilirsiniz. Daha fazla bilgi için [Hata Ayıklayıcı'nın uygulamanıza nasıl ekleyen daha iyi tanımak](../debugger/debugger-tips-and-tricks.md#modules_window).
 
##  <a name="BKMK_Find_symbol___pdb__files"></a> Burada, hata ayıklayıcı sembol dosyalarını aramak? 
  
1.  DLL veya yürütülebilir dosyanın içinde belirtilen konum.  
  
     (Varsayılan olarak, bilgisayarınızda bir DLL veya yürütülebilir dosya oluşturduysanız bağlayıcı, DLL veya yürütülebilir dosya içindeki ilgili .pdb dosyasının yolunu ve dosya adını tam olarak yerleştirir. Hata ayıklayıcı önce DLL'de veya yürütülebilir dosyada belirtilen konumda sembol dosyasının varolup olmadığını denetler. Her zaman bilgisayarınızda derlediğiniz kod için kullanılabilir semboller olduğundan bu yararlıdır.)  
  
2.  DLL veya yürütülebilir dosyayla aynı klasörde bulunan .pdb dosyaları.

3. Herhangi bir konum [hata ayıklayıcı ayarlarında belirtilen](#BKMK_Specify_symbol_locations_and_loading_behavior) sembol dosyaları için. 
  
    * Yerel sembol önbellek klasörleri.  
  
    * Tüm ağ, internet veya yerel sembol sunucuları ve (etkinse) Microsoft sembol sunucusu gibi belirtilir konumları. 

> [!NOTE]
> Visual Studio 2012 önce uzak bir cihazda yönetilen kod hata ayıklaması yaparken sembol dosyalarını uzak makinede gerekli. Visual Studio 2012'den itibaren tüm sembol dosyaları yerel makinede veya bir konumda bulunmalıdır [hata ayıklayıcı ayarlarında belirtilen](#BKMK_Specify_symbol_locations_and_loading_behavior).  
  
##  <a name="BKMK_Why_do_symbol_files_need_to_exactly_match_the_executable_files_"></a> Neden sembol dosyalarının yürütülebilir dosyalarla tam olarak eşleşmesi gerekiyor mu?  
Hata ayıklayıcı, yalnızca yürütülebilir dosya oluşturulduğunda, oluşturulan .pdb dosyasıyla tam olarak eşleşen bir yürütülebilir dosya için bir .pdb dosyasını yükler (yani, .pdb özgün olmalı veya özgün .pdb'nin kopyasını olmalıdır). Doğru ve verimli kod oluşturma olan temel görevinin yanı sıra derleyici derleme hızı için de optimize edilmiş olduğundan, kodun kendisi değişmese bile yürütülebilir dosyanın gerçek düzeni değişebilir. Daha fazla bilgi için [neden Visual Studio gerektiriyor hata ayıklayıcı sembol birlikte oluşturuldukları ikili dosyalarla tam olarak eşleşen dosyaları?](https://blogs.msdn.microsoft.com/jimgries/2007/07/06/why-does-visual-studio-require-debugger-symbol-files-to-exactly-match-the-binary-files-that-they-were-built-with/)
  
##  <a name="BKMK_Specify_symbol_locations_and_loading_behavior"></a> Hata ayıklayıcı sembol dosyaları ve sembol yükleme davranışı için burada görünür yapılandırın
 Visual Studio IDE içinde bir projede hata ayıklaması yaparken, hata ayıklayıcı proje dizininde yer alan sembol dosyalarını otomatik olarak yükler. Alternatif arama yolları belirtin ve Microsoft, Windows veya üçüncü taraf bileşenleri için Sembol sunucularını **Araçlar > Seçenekler > hata ayıklama > Semboller**. Hata ayıklayıcının sembolleri otomatik olarak istediğiniz belirli modülleri belirtebilirsiniz. Ve daha sonra etkin bir şekilde hata ayıklama yaparken bu ayarları el ile değiştirebilirsiniz.  
  
1.  Visual Studio'da açın **Araçlar > Seçenekler > hata ayıklama > Semboller** sayfası.  
  
     ![Araçlar &#45; seçenekleri &#45; hata ayıklama &#45; semboller sayfasını](../debugger/media/dbg_tools_options_symbols.gif "DBG_Tools_Options_Symbols")  
  
2.  Klasör Seç ![Araçları&#47; seçenekleri&#47; hata ayıklama&#47;sembolleri klasör simgesini](../debugger/media/dbg_tools_options_foldersicon.png "DBG_Tools_Options_FoldersIcon") simgesi. Düzenlenebilir metin görünür **sembol dosyası (.pdb) konumlar** kutusu.  
  
3.  URL'yi ya da sembol sunucusunun veya sembol konumunun dizin yolunu yazın. Deyimi tamamlama doğru biçimi bulmanıza yardımcı olur.

    Kullanabileceğiniz **Ctrl + Yukarı** ve **Ctrl + aşağı** simge konumları yüklenme sırasını değiştirmek için. Tuşuna **F2** bir URL düzenlenecek veya dizin yolu.
  
4.  Sembol geliştirmek için yükleme performansını yazın sembolleri kopyalanabildiği sembol sunucuları tarafından yerel bir dizin yolu **önbellek sembolleri bu dizinde** sembolleri kopyalanabilir yerel bir dizin kutusu.  
  
    > [!NOTE]
    >  Sembol önbelleğinizi korunan klasöre (C:\Windows folder veya bunun alt klasörlerinden biri) koymayın. Bunun yerine okuma-yazma klasörü kullanın.  
  
    > [!NOTE]
    >  C++ projeleri için _NT_SYMBOL_PATH ortam değişken kümesi varsa, altında ayarlanan değer kılar **önbellek sembolleri bu dizinde**.

### <a name="specify-symbol-loading-behavior"></a>Sembol yükleme davranışı belirtin 
  
Otomatik olarak yüklenmesini istediğiniz dosyaları belirtebilirsiniz **sembol dosyası (.pdb) konumlar** hata ayıklamaya başladığınızda kutusu konumlarından. Proje dizinindeki sembol dosyaları her zaman yüklenir.  
  
1.  Seçin **tüm modüllerin aktarılmadıysa** seçtiğinizde belirttiğiniz hariç tüm modüller için tüm sembolleri yüklemek üzere **dışlanan modülleri belirtin** bağlantı.  
  
2.  Seçin **yalnızca belirtilen modüller** seçeneğini ve ardından **modülleri belirtin** otomatik olarak yüklemek istediğiniz dosyaları sembol modülleri listelemek için. Diğer modüller için sembol dosyaları göz ardı edilir.  
  
### <a name="specify-additional-symbol-options"></a>Ek sembol seçenekleri belirtin 
  
Üzerinde şu seçenekler ayarlayabilirsiniz **Araçlar > Seçenekler > hata ayıklama > Genel** sayfası:  
  
**DLL dışarı aktarmaları (yalnızca yerel) yükle**  
  
Seçildiğinde, DLL dışa aktarma tablolarını yükler. DLL dışa aktarma tablolarının sembole yönelik bilgileri, Windows iletileri, Windows yordamları (WindowProcs), COM nesneleri veya sıralama ile ya da sembolleri olmayan herhangi bir DLL ile çalışıyorsanız yararlı olabilir. DLL dışa aktarma bilgilerini okuma bazı ek okumalar içerir. Bu nedenle, bu özellik varsayılan olarak kapalıdır.  
  
Bir DLL'nin dışa aktarma tablosunda hangi sembollerin kullanılabilir görmek için `dumpbin /exports`. Semboller tüm 32-bit sistem DLL için kullanılabilir. Okuyarak `dumpbin /exports` çıkışı, alfasayısal olmayan karakterler de dahil tam işlev adını görebilirsiniz. Bu, bir işlev bir kesme noktası ayarlamak için yararlıdır. DLL dışarı aktarma tablolarındaki işlev adları, hata ayıklayıcının başka bir yerinde kesilmiş görünebilir. Aramalar geçerli işlev en üstte (en yoğun şekilde iç içe geçmiş) olacak şekilde arama sırasıyla listelenir. Daha fazla bilgi için [dumpbin/EXPORTS](/cpp/build/reference/dash-exports).  
  
###  <a name="BKMK_Use_symbol_servers_to_find_symbol_files_not_on_your_local_machine"></a> Yerel makinenizde olmayan sembol dosyalarını bulmak için Sembol sunucularını kullanın  
 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] hata ayıklama sembol dosyalarını symsrv protokolünü uygulayan sembol sunucularından indirebilirsiniz. [Visual Studio Team Foundation Server](http://msdn.microsoft.com/Library/bd6977ca-e30a-491a-a153-671d81222ce6) ve [Windows için hata ayıklama araçları](http://msdn.microsoft.com/library/windows/hardware/ff551063\(v=VS.85\).aspx) , sembol Hizmetleri uygulayan iki araçtır. VS kullanılacak sembol sunucularını belirtirsiniz **seçenekleri** iletişim kutusu.  
  
 Kullanabileceğiniz sembol sunucuları şunlardır:  
  
 **Microsoft Genel sembol sunucuları**  
  
 Bir sistem DLL dosyasına veya bir üçüncü taraf kitaplığına yapılan bir çağrı sırasında oluşan bir çökme hatasını gidermek için, genellikle Windows DLL'leri, EXE'ler, ve cihaz sürücüleri için semboller içeren .pdb dosyalarına gereksinim duyarsınız. Bu sembolleri Microsoft ortak sembol sunucularından elde edebilirsiniz. Microsoft Genel sembol sunucuları, MDAC, IIS, ISA ek olarak Windows işletim sistemleri için semboller sağlar ve [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)].  
  
 Microsoft sembol sunucuları kullanmayı tercih **seçenekler ve ayarlar** üzerinde **hata ayıklama** menüsünü seçip **sembolleri**. Seçin **Microsoft sembol sunucuları**.  
  
 **Bir iç ağdaki veya yerel makinenizdeki sembol sunucuları**  
  
 Ekibiniz veya şirketiniz, kendi ürünleriniz için ve dış kaynaklardan alınan sembollerin önbelleği olarak sembol sunucuları oluşturabilir. Kendi makineniz üzerinde bir sembol sunucusu olabilir. Bir URL veya yol olarak sembol sunucularının konumunu girin **hata ayıklama**/**sembolleri** VS sayfası **seçeneği iletişim**.  
  
 **Üçüncü taraf sembol sunucuları**  
  
 Üçüncü taraf Windows uygulamaları ve kitaplıkları sağlayıcılar internet üzerinden sembol sunucusuna erişim sağlayabilir. Bu sembol sunucularının URL'sini de girin **hata ayıklama**/**sembolleri** sayfası  
  
> [!NOTE]
>  Microsoft ortak sembol sunucularından farklı bir sembol sunucusu kullanıyorsanız, sembol sunucusunun ve yolunun güvenilir olduğundan emin olun. Sembol dosyası rastgele yürütülebilir kod içerebileceğinden güvenlik tehditlerine maruz kalabilirsiniz.  
  
###  <a name="BKMK_Find_and_load_symbols_while_debugging"></a> Bulma ve hata ayıklama sırasında sembolleri yükle  
 Hata ayıklayıcı kesme modundayken, hata ayıklayıcı seçenekleriyle daha önce hariç tutulan veya derleyicinin bulamadığı bir modül için semboller yükleyebilirsiniz. Çağrı Yığını, Modüller, Yereller, Otolar ve tüm Gözcü pencerelerinin kısayol menülerinden sembol yükleyebilirsiniz. Hata ayıklayıcısı sembol veya kaynak dosyalarına sahip olmayan kodu keserse, bir belge penceresi görüntülenir. Burada, eksik dosyaları ve bunları bulup yüklemek için yapılacak eylemler hakkında bilgi bulabilirsiniz.
  
 **Yüklü sembol yok belge sayfaları içeren sembolleri bulun**  
  
 Hata ayıklayıcının kullanılabilir sembolleri bulunmayan kodlara girebilmesi için çeşitli yollar vardır:  
  
1.  Kodun içine adımlama.  
  
2.  Kodu kesme noktasından veya özel durumdan ayırma.  
  
3.  Farklı bir iş parçacığına geçiş.  
  
4.  Çağrı Yığını penceresinde bir çerçeveyi çift tıklayarak yığın çerçevesini değiştirme.  
  
 Bu olaylardan biri oluştuğunda, hata ayıklayıcı görüntüler **yüklü sembol yok** gerekli sembolleri bilip yardımcı olması için sayfa.  
  
 ![Yüklü sembol yok sayfası](../debugger/media/dbg_nosymbolsloaded.png "DBG_NoSymbolsLoaded")  
  
-   Arama yollarını değiştirmek için seçilmeyen bir yolu seçin veya **yeni** ve yeni bir yol girin. Seçin **yük** yolları tekrar aramak ve bulunursa sembol dosyasını yüklemek için.  
  
-   Seçin **Gözat ve Bul**_yürütülebilir dosya adı_**...**  herhangi bir sembol seçeneklerini geçersiz kılmak ve arama yollarını yeniden deneyin. Sembol dosyası bulunursa yüklenir veya sembol dosyasını el ile seçmeniz için bir Dosya Gezgini görüntülenir.  
  
-   Seçin **sembol ayarlarını değiştir...**  görüntülenecek **hata ayıklama** > **sembolleri** VS Seçenekleri iletişim kutusu sayfası.  
  
-   Seçin **ayrıştırılmış kodu görüntüle** yeni bir pencerede bir defa ayrıştırılmış kodu göstermek için.  
  
-   Kaynak veya sembol dosyaları bulunamadığında ayrıştırılmış kodu her zaman göstermek için seçin **Seçenekleri iletişim kutusu** bağlantısını ve her ikisini de seçin **adres seviyesinde hata ayıklamayı etkinleştir** ve **ayrıştırılmış Kodu Göster, Kaynak kullanılamıyor**.  
  
     ![Seçenekleri &#47; hata ayıklama &#47; genel ayrıştırma seçenekleri](../debugger/media/dbg_options_general_disassembly_checkbox.png "DBG_Options_General_disassembly_checkbox")  
  
 **Sembol seçeneklerini kısayol menüsünden değiştirme**  
  
 Kesme modunda çalışırken, Çağrı Yığını, Modüller, Yerel Öğeler, Otomatik Öğeler ve tüm İzleme pencerelerinde görüntülenen öğelerin sembollerini bulabilir ve yükleyebilirsiniz. Pencerede bir öğe seçin, kısayol menüsünü açın ve aşağıdaki seçeneklerden birini seçin:  
  
|Seçenek|Açıklama|  
|------------|-----------------|  
|**Sembolleri yükle**|Belirtilen konumlardan sembolleri yüklemeye çalışır **hata ayıklama**/**sembolleri** sayfasının **seçenekleri** iletişim kutusu. Sembol dosyası bulunamazsa, Dosya Gezgini başlatılır, bu sayede aranacak yeni bir konum belirtebilirsiniz.|  
|**Sembol yükleme bilgisi**|Yüklenen sembol dosyasının konumunu veya hata ayıklayıcı dosyasını bulamazsanız, aranan konumları gösteren bilgiler sunar.|  
|**Sembol ayarları...**|Açılır **hata ayıklama**/**sembolleri** VS sayfası **seçenekleri** iletişim kutusu.|  
|**Her zaman otomatik olarak yükle**|Hata ayıklayıcı tarafından otomatik yüklenen dosya listesine sembol dosyası ekler.|  
  
###  <a name="BKMK_Set_compiler_options_for_symbol_files"></a> Sembol dosyaları için derleyici seçeneklerini ayarlama  
VS IDE'den projenizi ne zaman ve standart **hata ayıklama** yapı yapılandırması C++ ve yönetilen derleyiciler kodunuz için uygun semboller dosyalarını oluşturun. Sembol dosyaları oluşturmak için komut satırında derleyici seçeneklerini de ayarlayabilirsiniz.  
  
**C++ seçenekleri**  
  
Program veritabanı (.pdb) dosyası, hata ayıklamayı ve programınızın Hata ayıklama yapılandırmasının artımlı bağlamasına olanak tanıyan proje durum bilgilerini tutar. İle oluşturduğunuzda .pdb dosyası oluşur [/zı veya /Zi](/cpp/build/reference/z7-zi-zi-debug-information-format) (C/C++ için).  
  
İçinde [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)], [/Fd](/cpp/build/reference/fd-program-database-file-name) seçeneği derleyici tarafından oluşturulan .pdb dosyasını adlandırır. Bir proje oluşturduğunuzda, [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] sihirbazları kullanarak **/Fd** seçeneği adlı bir .pdb dosyası oluşturmak için ayarlanır *proje*.pdb.  
  
C/C++ uygulamanızı bir derleme görevleri dosyası derleme ve belirtirseniz **/zi** veya **/zi** olmadan **/Fd**, iki .pdb dosyası ile biter:  
  
* VC*x*.pdb, burada *x* Visual C++ sürümlerinden birini, örneğin vc11.pdb öğesini temsil eder. Bu dosya, tek tek OBJ dosyaları için hata ayıklama bilgilerini depolar ve proje derleme görevleri dosyası ile aynı dizinde bulunur.  
  
* Project.pdb bu dosya the.exe dosyası için tüm hata ayıklama bilgilerini depolar. C/C++'ta \debug alt dizininde bulunur.  
  
Her OBJ dosyası oluşturduğunda, C/C++ derleyicisi hata ayıklama bilgileri VC birleştirir.*x*.pdb. Eklenen bilgiler türü bilgilerini içerir, ancak işlev tanımları gibi sembol bilgilerini içermez. Her kaynak dosyası gibi ortak başlık dosyaları gibi içerse bile bunu \<windows.h >, bir başlıklardan her OBJ dosyasında olmak yerine yalnızca bir kez saklanır.  
  
Bağlayıcı, projenin EXE dosyasına ilişkin hata ayıklama bilgilerini içeren project.pdb'yi oluşturur. Project.pdb dosyası VC bulunan tür bilgilerini değil, işlev prototipleri dahil olmak üzere tam hata ayıklama bilgilerini içeren*x*.pdb. Her iki .pdb dosyası da artımlı güncelleştirmelere izin verir. Bağlayıcı ayrıca .pdb dosyasının yolunu, oluşturduğu .exe veya .dll dosyasına katıştırır.  
  
[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Hata ayıklayıcısı yolu EXE veya DLL dosyasında .pdb dosyasının project.pdb dosyasını bulmak için kullanır. Hata ayıklayıcısı .pdb dosyasını bu yerde bulunamıyor veya yol geçersizse (örneğin, proje başka bir bilgisayara taşınmışsa) hata ayıklayıcı EXE içeren yolu arar ve sembol yollarını arar **seçenekleri** iletişim kutusu (**hata ayıklama** klasöründe **sembolleri** düğümü). Hata ayıklayıcı, hata ayıklaması yapılan yürütülebilir öğeyle eşleşmeyen bir .pdb dosyası yüklemez. Hata ayıklayıcı bir .pdb dosyası bulamazsa, bir **sembol Bul** iletişim kutusu görüntülenir, burada sembol arayabilir veya arama yoluna ilave konum ekleyebilirsiniz.  
  
**.NET framework seçenekleri**  
  
Program veritabanı (.pdb) dosyası, hata ayıklamayı ve programınızın hata ayıklama yapılandırmasının artımlı bağlamasına olanak tanıyan proje durum bilgilerini tutar. İle oluşturduğunuzda .pdb dosyası oluşur **/debug**. İle uygulama oluşturabilirsiniz **/Debug: Full** veya **/debug:pdbonly**. İle oluşturma **/Debug: Full** hata ayıklaması yapılabilir kod oluşturur. İle oluşturma **/debug:pdbonly** .pdb dosyaları oluşturur ancak oluşturmaz `DebuggableAttribute` JIT derleyicisine hata ayıklama bilgilerinin kullanılabilir olduğunu bildirir. Kullanım **/debug:pdbonly** hata ayıklanabilir olmasını istemediğiniz yayın yapısı için .pdb dosyaları oluşturmak istiyorsanız. Daha fazla bilgi için [/Debug (C# Derleyici Seçenekleri)](/dotnet/csharp/language-reference/compiler-options/debug-compiler-option) veya [/Debug (Visual Basic)](/dotnet/visual-basic/reference/command-line-compiler/debug).  
  
[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Hata ayıklayıcısı yolu EXE veya DLL dosyasında .pdb dosyasının project.pdb dosyasını bulmak için kullanır. Hata ayıklayıcısı .pdb dosyasını bu yerde bulunamıyor veya yol geçersizse, hata ayıklayıcı EXE içeren yolu arar ve sembol yollarını sonra belirtilen **seçenekleri** iletişim kutusu. Bu yol genellikle **hata ayıklama** klasöründe **sembolleri** düğümü. Hata ayıklayıcı, hata ayıklaması yapılan yürütülebilir dosyayla eşleşmeyen bir .pdb dosyası yüklemez. Hata ayıklayıcı bir .pdb dosyası bulamazsa, bir **sembol Bul** iletişim kutusu görüntülenir, burada sembol arayabilir veya arama yoluna ilave konum ekleyebilirsiniz.  
  
**Web uygulamaları**  
  
Uygulamanızın yapılandırma dosyası (Web.config) hata ayıklama moduna ayarlanmalıdır. Hata ayıklama modu ASP.NET'in dinamik olarak oluşturulan dosyalar için sembol oluşturmasına neden olur ve hata ayıklayıcının ASP.NET uygulamasına eklemesine olanak tanır. Visual Studio hata ayıklamak başlattığınızda Web proje şablonunu projenizi oluşturduysanız bu otomatik olarak ayarlar.  
  
##  <a name="BKMK_Find_source_files"></a> Kaynak dosyaları bulun  
  
###  <a name="BKMK_Where_the_debugger_searches_for_source_files"></a> Hata ayıklayıcı kaynak dosyaları nerede arar  
 Hata ayıklayıcı kaynak dosyaları aşağıdaki konumlarda arar:  
  
1.  Hata ayıklayıcı tarafından başlatılan Visual Studio örneğinin IDE'si içinde açık olan dosyalar.  
  
2.  Visual Studio örneğinde açık olan Çözümdeki dosyalar.  
  
3.  Belirtilen dizinleri **ortak özellikler**/**kaynak dosyalarında Hata Ayıkla** çözüm özellikleri sayfasında. (İçinde **Çözüm Gezgini**, çözüm düğümüne sağ tıklayın ve Seç'i seçin **özellikleri**. )  
  
4.  Modülün .pdb dosyasının kaynak bilgisi. Bu, modül oluşturulduğunda kaynak dosyanın konumu olabileceği gibi, bir kaynak sunucuya ilişkin komut da olabilir.  
  
###  <a name="BKMK_Find_and_load_source_files_with_the_No_Source___No_Symbols_Loaded_pages"></a> Bilip yüklemenize Source/No sembol yüklenmedi sayfalarıyla kaynak dosyaları  
 Hata ayıklayıcı kaynak dosyasının olmadığı yerde yürütmeyi keserse, görüntüler **yüklü kaynak yok** veya **yüklü sembol yok** yardımcı olabilecek sayfaları kaynak dosyasını bulmaya. **Yüklü sembol yok** hata ayıklayıcı, arama işlemini tamamlamak üzere yürütülebilir dosya için bir simge (.pdb) dosyası bulamadığında görünür. Sembol Yok sayfası dosyayı aramak için seçenekler sağlar. Seçeneklerden birini yürütün ve hata ayıklayıcı semboller dosyasındaki bilgileri kullanarak kaynak dosyayı alabilir sonra .pdb bulunursa, kaynak görüntülenir. Aksi takdirde, bir **yüklü kaynak yok** sorunu açıklayan sayfası görüntülenir. Sayfa, sorunu giderebilecek eylemleri gerçekleştirebilen seçenek bağlantıları görüntüler.  
  
###  <a name="BKMK_Add_source_file_search_paths_to_a_solution"></a> Kaynak dosyası arama yollarını çözüme ekleme  
 Kaynak dosyalarını aramak için ağ veya yerel dizin belirtebilirsiniz.  
  
1.  Çözüm Gezgini içindeki çözümü seçin ve ardından **özellikleri** kısayol menüsünden.  
  
2.  Altında **ortak özellikler** düğümünü seçin **kaynak dosyalarında Hata Ayıkla**.  
  
3.  Klasörü tıklatın ![Araçları&#47; seçenekleri&#47; hata ayıklama&#47;sembolleri klasör simgesini](../debugger/media/dbg_tools_options_foldersicon.png "DBG_Tools_Options_FoldersIcon") simgesi. Düzenlenebilir metin görünür **kaynak kodu içeren dizinler** listesi.  
  
4.  Aramak istediğiniz yolu ekleyin.  
  
 Yalnızca belirtilen dizin arandığına dikkat edin. Arama yapmak istediğiniz alt dizinler için girdi eklemeniz gerekir.  
  
###  <a name="BKMK_Use_source_servers"></a> Kaynak sunucuları kullanma  
 Yerel makinede kaynak kod olmadığında veya .pdb dosyası kaynak kodla eşleşmediğinde, uygulamada hata ayıklamaya yardımcı olması için Kaynak Sunucuyu kullanabilirsiniz. Kaynak Sunucu, dosya isteklerini alır ve gerçek dosyaları döndürür. Kaynak Sunucu, srcsrv.dll adlı bir DLL dosyası ile çalışır. Kaynak Sunucu, kaynak kodu depodan almak için kullanılan komutların yanı sıra kaynak kodu deposuna işaretçiler içeren uygulamanın .pdb dosyasını okur. devenv.exe ve srcsrv.dll ile aynı dizine konması gereken srcsrv.ini adlı dosyadaki izin verilen komutları listeleyerek hangi komutlara uygulamanın .pdb dosyasından yürütülmesini izin verileceğini sınırlayabilirsiniz.  
  
> [!IMPORTANT]
>  Rastgele komutlar uygulamanın .pdb dosyasına katıştırılabildiğinden yalnızca yürütmek istediğiniz komutları srcsrv.ini dosyasına koyduğunuzdan emin olun. srcsvr.ini dosyasında olmayan bir komutu yürütme girişimi, bir onay iletişim kutusunun görüntülenmesine neden olur. Daha fazla bilgi için [güvenlik uyarısı: hata ayıklayıcı gerekir yürütme güvenilmeyen komut](../debugger/security-warning-debugger-must-execute-untrusted-command.md). Komut parametrelerinde bir doğrulama yapılmadı, bu nedenle güvenilir komutlara dikkat edin. Örneğin, cmd.exe'ye güvendiyseniz, kötü niyetli bir kullanıcı, komutu tehlikeli duruma getirecek parametreler belirtebilir.  
  
 **Bir kaynak sunucusunun kullanımını etkinleştirmek için**  
  
1.  Önceki bölümde açıklanan güvenlik önlemleri ile derlediğinizden emin olun.  
  
2.  Üzerinde **Araçları** menüsünde seçin **seçenekleri**.  
  
     **Seçenekleri** iletişim kutusu görüntülenir.  
  
3.  İçinde **hata ayıklama** düğümünü seçin **genel**.  
  
4.  Seçin **kaynak sunucusu desteğini etkinleştir** onay kutusu.  
  
     ![Kaynak sunucu seçenekleri etkinleştirme](../debugger/media/dbg_options_general_enablesrcsrvr_checkbox.png "DBG_Options_General_EnableSrcSrvr_checkbox")  
  
5.  (İsteğe bağlı) İstediğiniz alt seçeneği belirleyin.  
  
     Unutmayın hem **kısmi güven derlemeleri (sadece yönetilen) için kaynak sunucuya izin ver** ve **her zaman sormadan güvenilmeyen kaynak sunucu komutlarını Çalıştır** yukarıda açıklanan güvenlik risklerini artırabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
[Sembol dosyaları ve Visual Studio sembol Ayarları'nı anlama](https://blogs.msdn.microsoft.com/devops/2015/01/05/understanding-symbol-files-and-visual-studios-symbol-settings/)

[Visual Studio 2012 ve 2013 değişiklikleri yükleme .NET uzaktan sembolü](https://blogs.msdn.microsoft.com/devops/2013/10/16/net-remote-symbol-loading-changes-in-visual-studio-2012-and-2013/)
