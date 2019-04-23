---
title: XML komut tablosu tasarlama (. Vsct) dosyaları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT files, designing
ms.assetid: bb87a322-bac4-4258-92bc-9a876f05d653
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1e70a64e01e388af61127fd76f4a2fcee8e5a9b9
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60091570"
---
# <a name="design-xml-command-table-vsct-files"></a>XML komut tablosu (.vsct) dosyaları tasarlama
Bir XML komut tablosu (*.vsct*) dosya VSPackage için komut öğelerin Görünüm ve düzeninin açıklar. Düğmeler, birleşik giriş kutuları, menüler, araç çubukları ve grupları komut öğelerinin komut öğeler içerir. Bu makalede, XML komut tablosu dosyaları, komut öğeleri ve menüler nasıl etkilediklerini ve bunların nasıl oluşturulacağı açıklanır.

## <a name="commands-menus-groups-and-the-vsct-file"></a>Komutlar, menüler, grupları ve .vsct dosyası
 *.Vsct* dosyaları komutlar, menüler ve komut gruplarını düzenlenmiştir. XML etiketleri içinde *.vsct* dosya her birinde öğe birlikte komut düğmeleri, komut yerleştirme ve bit eşlemler gibi diğer ilişkili öğeleri temsil eder.

 Çalıştırarak yeni bir VSPackage'ı oluşturduğunuzda [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] paketi şablonu şablon oluşturur bir *.vsct* gerekli öğeler dosyasıyla bir menü komutu, araç penceresi veya seçimlerinize bağlı olarak, özel bir düzenleyici. Bu *.vsct* dosya daha sonra değiştirilebilir belirli bir VSPackage gereksinimlerini karşılamak için. Değiştirme örnekleri için bir *.vsct* bkz [genişletmek menüler ve komutlar](../../extensibility/extending-menus-and-commands.md).

 Yeni bir oluşturmak için boş *.vsct* bkz [nasıl yapılır: Oluşturma bir *.vsct* dosya](../../extensibility/internals/how-to-create-a-dot-vsct-file.md). XML öğeleri, öznitelikleri ve değerleri oluşturulduktan sonra komut öğesi düzeni tanımlamak için dosyaya ekleyin. Ayrıntılı bir XML şeması için bkz: [VSCT XML Şeması Başvurusu](../../extensibility/vsct-xml-schema-reference.md).

## <a name="differences-between-ctc-and-vsct-files"></a>.Ctc ve .vsct dosyaları arasındaki farklar
 Anlamı XML arkasında bulunan etiketleri sırada bir *.vsct* dosya, bu etiketler artık kullanım dışı olarak aynı *.ctc* dosya biçimi, geliştirdikleri biraz farklıdır:

- Yeni  **\<extern >** etikettir burada diğer başvuru *.h* dosyaları için bu dosyaları gibi derlenecek [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] araç çubuğu.

- Sırada *.vsct* destek dosyaları **/ include** deyimi olarak *.ctc* dosyaları, ayrıca yeni özellikleri  **\<Al >** öğe. Fark, **/ include** getirir *tüm* bilgileri sırada  **\<Al >** adları yalnızca getirir.

- Sırada *.ctc* dosyalar gerektirir, önişlemci yönergeleri tanımladığınız bir başlık dosyası, gerekli değil *.vsct* dosyaları. Bunun yerine, yönergeleri bulunan sembol tablosu yerleştirin  **\<Sembol >** alt kısmında bulunan öğeleri *.vsct* dosya.

- *.vsct* dosyaları özelliği bir  **\<ek açıklama >** istediğiniz notları veya hatta resimler gibi herhangi bir bilgi eklemeye izin veren bir etiket.

- Değerler, öğenin öznitelikleri olarak depolanır.

- Komut bayrakları ayrı ayrı depolanır veya yığın.  Ancak, IntelliSense, yığılmış komut bayrakları çalışmaz. Komut bayrakları hakkında daha fazla bilgi için bkz: [CommandFlag öğesi](../../extensibility/command-flag-element.md).

- Bölünmüş bırakmalar, combos vb. gibi birden çok tür belirtebilirsiniz.

- GUID'ler doğrulamaz.

- Her kullanıcı Arabirimi öğesi ile görüntülenen metinleri temsil eden bir dize var.

- Üst isteğe bağlıdır. Atlanırsa, değer *grubu bilinmeyen* kullanılır.

- *Simgesi* bağımsız değişken isteğe bağlıdır.

- Bit eşlem bölüm: Bu bölümde de aynı olan bir *.ctc* artık bir dosya adı tarafından çekilir içinde Href aracılığıyla belirtebilirsiniz dışında dosya *vsct.exe* derleyici derleme zamanında.

- ResID: Eski kaynak kimliği kullanılan ve hala çalıştığı aynı olabilir bit eşlem *.ctc* dosyaları.

- HRef: Bit eşlem kaynağı için bir dosya adı belirtmenizi sağlar bir yeni yöntem. Kullanılan bölümüne atlayabilirsiniz. böylece tüm kullanılan olduğunu varsayar. Derleyicinin varsayılan dosya, sonra tüm ağ paylaşımları üzerindeki yerel kaynakları için arar ve tüm kaynakları tarafından tanımlanan **/I** geçin.

- Tuş: Artık bir öykünücü belirtmeniz gerekmez. Bir belirtirseniz, derleyicinin düzenleyici ve öykünücü aynı olduğu varsayılır.

- Keychord: Keychord bırakıldı. Yeni biçim *Key1, Değişiklik1, Key2, Mod2*.  Bir karakter, onaltılık veya VK sabiti belirtebilirsiniz.

Yeni derleyici *vsct.exe*, her ikisi de derler *.ctc* ve *.vsct* dosyaları. Eski *ctc.exe* derleyici, ancak tanımıyor veya derleme *.vsct* dosyaları.

Kullanabileceğiniz *vsct.exe* varolan dönüştürmek için derleyici *.cto* dosyasını bir *.vsct* dosya. Daha fazla bilgi için [nasıl yapılır: Mevcut bir .cto dosyadan .vsct dosyası oluşturma](../../extensibility/internals/how-to-create-a-dot-vsct-file.md#how-to-create-a-dot-vsct-file-from-an-existing-dot-cto-file).

## <a name="the-vsct-file-elements"></a>.Vsct dosyası öğeleri
 Komut tablosu aşağıdaki hiyerarşi ve öğeleri sahiptir:

- [CommandTable öğesi](../../extensibility/commandtable-element.md): Tüm komutlar, menü grupları ve menüler VSPackage'ı ile ilişkili temsil eder.

- [Extern öğesi](../../extensibility/extern-element.md): Birleştirmek istediğiniz herhangi bir dış .h dosyaları başvuran *.vsct* dosya.

- [Öğe dahil](../../extensibility/include-element.md): İle birlikte derlemek istediğiniz herhangi bir ek üstbilgi (.h) dosyalarına başvuran, *.vsct* dosya. A *.vsct* dosya içerebilir *.h* komutlarını, menü grupları ve menüler IDE veya başka bir VSPackage sağlayan tanımlayan sabitler içeren dosya.

- [Commands öğesi](../../extensibility/commands-element.md): Tüm yürütülebilecek tek tek komutlarla temsil eder. Her komut aşağıdaki dört alt öğeleri içerir:

- [Menus öğesi](../../extensibility/menus-element.md): Tüm menüleri ve araç çubuklarını VSPackage'ı temsil eder. Menü komutları grupları için kapsayıcılardır.

- [Groups öğesi](../../extensibility/groups-element.md): Tüm grupları VSPackage'ı temsil eder. Grupları tek tek komutlarla koleksiyonlarıdır.

- [Buttons öğesi](../../extensibility/buttons-element.md): Tüm komut düğmeleri ve menü öğeleri VSPackage'ı temsil eder. Düğme komutları ile ilişkilendirilebilen visual denetimlerdir.

- [Bitmaps öğesi](../../extensibility/bitmaps-element.md): Tüm bit eşlemler tüm düğmelerin VSPackage'ı temsil eder. Bit eşlemler yanındaki veya bağlama komut düğmeleri görüntüleme resimleri ' dir.

- [CommandPlacements öğesi](../../extensibility/commandplacements-element.md): Özel komutlar, VSPackage menülerde burada tarihli ek konumlarını gösterir.

- [VisibilityConstraints öğesi](../../extensibility/visibilityconstraints-element.md): Bir komut hiç zaman ya da belirli bir iletişim kutusu veya pencere görüntülendiğinde gibi yalnızca belirli bağlamlarda, görüntüler olup olmadığını belirtir. Belirtilen bağlamı etkin olduğunda, menüler ve bu öğe için bir değere sahip komutlar görüntülenir. Komutu her zaman görüntülemek için varsayılan davranıştır.

- [KeyBindings öğesi](../../extensibility/keybindings-element.md): Komutlar için herhangi bir tuş bağlamaları belirtir. Gibi bir komut yürütmek için basılması gereken diğer bir deyişle, bir veya daha fazla anahtar birleşimlerini **Ctrl**+**S**.

- [UsedCommands öğesi](../../extensibility/usedcommands-element.md): Bildirir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ortamı geçerli VSPackage'ı etkin olduğunda belirtilen komut başka kod tarafından uygulanan olsa da, bu komutu uygulamasını sağlar.

- [Symbols öğesi](../../extensibility/symbols-element.md): Komutlarınızın paketteki tüm GUID kimlikleri ve sembol adlarını içerir.

## <a name="vsct-file-design-guidelines"></a>.vsct dosyası tasarım yönergeleri
 Başarıyla tasarım bir *.vsct* dosyasında, aşağıdaki yönergeleri izleyin.

- Komutları yalnızca gruplarda bulunabilecek gruplar yalnızca menülerde yerleştirilebilir ve menüler yalnızca gruplarında yerleştirilebilir. Yalnızca menüler IDE, gruplar aslında görüntülenir ve komutları değildir.

- Alt menüye doğrudan atanamaz ancak menüye sırayla atandığı bir gruba atanması gerekir.

- Bir ana öğe grubu veya üst alanın kendi tanımlayan yönergesi kullanarak menü komutları, alt menüler ve gruplar atanabilir.

- Bir komut tablosu yalnızca yönergeleri üst alanları düzenleme önemli sınırlama vardır. Nesneleri tanımlayan yönergeleri, yalnızca bir üst bağımsız değişken alabilir.

- Komutları, grupları veya alt menüler yeniden kullanmak, kendi ile nesnesinin yeni bir örneğini oluşturmak için yeni bir yönerge kullanılmasını gerektiren `GUID:ID` çifti.

- Her `GUID:ID` çifti benzersiz olmalıdır. Örneğin, bir araç çubuğunda bir menü veya bağlam menüsünde yerleştirilen bir komutu yeniden tarafından işlenir <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> arabirimi.

- Komutlar ve alt menülere de atanabilir birden çok gruba ve grupları kullanarak birden çok menüleri atanabilir [komutlar öğenin](../../extensibility/commands-element.md).

## <a name="vsct-file-notes"></a>.vsct dosyası notları
 Herhangi bir değişiklik yaparsanız bir *.vsct* dosya derlemeniz hem yerel bir uydu DLL yerleştirin sonra çalıştırmalısınız **devenv.exe/Setup /nosetupvstemplates**. Bunu zorlar Deneysel kayıt defterini okunmasına ve açıklayan iç veritabanını belirtilen VSPackage kaynakları yapılması [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] derlenmeye.

 Geliştirme sırasında oluşturulması ve IDE kafa karıştırıcı dağınıklığı açabilir Deneysel kayıt defteri kovanında kayıtlı VSPackage birden çok proje için mümkündür. Bu sorunu gidermek için Deneysel hive tüm kayıtlı VSPackages ve IDE yaptığınız değişiklikleri kaldırmak için varsayılan ayarları sıfırlayabilirsiniz. Deneysel hive sıfırlamak için Visual Studio SDK ile birlikte gelen CreateExpInstance.exe aracını kullanın. Adresinden bulabilirsiniz:

 *% PROGRAMFILES (x 86) %\Visual Studio\\\<sürüm > SDK\VisualStudioIntegration\Tools\Bin\CreateExpInstance.exe*

 Komutunu kullanarak aracı çalıştırın **Createexpınstance reset**. Bu araç normalde ile yüklenen tüm kayıtlı VSPackages Deneysel kovanından kaldırır unutmayın [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

## <a name="see-also"></a>Ayrıca bkz.
- [Menüler ve komutlar genişletme](../../extensibility/extending-menus-and-commands.md)