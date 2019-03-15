---
title: ClangCompile görev | Microsoft Docs
ms.date: 03/10/2019
ms.topic: reference
f1_keywords:
- vc.task.clangcompile
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), ClangCompile task
- ClangCompile task (MSBuild (Visual C++))
author: mikeblome
ms.author: Michael.Blome
ms.workload:
- multiple
ms.openlocfilehash: 05843f3deec46dc790e0a5bee761abbad7ae1552
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58071152"
---
# <a name="clangcompile-task"></a>ClangCompile görevi

Visual C++ Derleyici aracı sarmalar clang.exe.

## <a name="parameters"></a>Parametreler

Parametreleri aşağıdaki tabloda açıklanmıştır **ClangCompile** görev.

|Parametre|Açıklama|
|---------------|-----------------|
|**AdditionalIncludeDirectories**|İsteğe bağlı **string []** parametresi.<br/><br/>Ekleme yoluna eklenecek bir veya daha fazla dizin belirtir; birden fazla ise noktalı virgülle ayırın.<br/><br/>Kullanım `-I[path]`.|
|**AdditionalOptions**|İsteğe bağlı **dize** parametresi.|
|**BufferSecurityCheck**|İsteğe bağlı **dize** parametresi.<br/><br/>Güvenlik denetimi, yığın arabelleği üst çalışır, bir ortak bir saldırı denemesi bir programın güvenlik algılamaya yardımcı olur. <br/><br/>Kullanım `fstack-protector`.|
|**BuildingInIde**|İsteğe bağlı **bool** parametresi.|
|**CLanguageStandard**|İsteğe bağlı **dize** parametresi.<br/><br/>C dil standardını belirler.<br/><br/>Kullanım `std=[value]` değeriyle **c89**, **c99**, **c11**, **gnu99**, veya **gnu11**.|
|**ClangVersion**|İsteğe bağlı **dize** parametresi.|
|**CompileAs**|İsteğe bağlı **dize** parametresi.<br/><br/>.C ve .cpp dosyaları için derleme dili tercihini seçin. Varsayılan, bağlı olarak .c veya .cpp uzantı algılar.<br/><br/>Kullanım `-x c`, `-x c++`.|
|**CppLanguageStandard**|İsteğe bağlı **dize** parametresi.<br/><br/>C++ dil standardını belirler.<br/><br/>Kullanım `std=[value]` değeriyle **c ++ 98**, **c ++ 11**, **c ++ 1y**, **gnu ++ 98**, **gnu ++ 11**, veya **gnu ++ 1y**.|
|**DataLevelLinking**|İsteğe bağlı **bool** parametresi.<br/><br/>Kullanılmayan verileri her veri öğesini ayrı bir bölümde çıkarma yoluyla kaldırarak yapılan bağlayıcı iyileştirmelerine sağlar.|
|**DebugInformationFormat**|İsteğe bağlı **dize** parametresi.<br/><br/>Derleyici tarafından oluşturulan hata ayıklama bilgilerinin türünü belirtir.<br/><br/>**Hiçbiri**, derleme daha hızlı olacak şekilde, hata ayıklama bilgisi üretir (kullanın `g0`).<br/>**FullDebug**, DWARF2 hata ayıklama bilgileri oluşturur (kullanın `g2 -gdwarf-2`).<br/>**LineNumber**, yalnızca satır numarası bilgisi oluştur (kullanın `gline-tables-only`).|
|**EnableNeonCodegen**|İsteğe bağlı **bool** parametresi.<br/><br/>NEON kayan nokta donanımı için kod oluşturmayı etkinleştirir. Bu, yalnızca arm mimarisi için geçerlidir.|
|**ExceptionHandling**|İsteğe bağlı **dize** parametresi.<br/><br/>Derleyici tarafından kullanılması için özel durum işleme modelini belirtir.<br/><br/>**Devre dışı bırakılmış**, özel durum işlemeyi devre dışı bırakmak (kullanın `fno-exceptions`).<br/>**Etkin**, özel durum işlemeyi etkinleştirin (kullanın `fexceptions`).<br/>**UnwindTables**, gerekli tüm statik verileri oluşturur, ancak oluşturulan kodu etkilemez (kullanın `funwind-tables`).|
|**FloatABI**|İsteğe bağlı **dize** parametresi.<br/><br/>Kayan nokta ABI'sini seçmek için seçenek.<br/><br/>**yazılım**, içeren kitaplık çağrıları kayan nokta işlemleri için çıktı oluşturmak derleyicinin (kullanın `mfloat-abi=soft`).<br/>**softfp**, donanım kayan nokta yönergeleri kullanan kod oluşturulmasını sağlar, ancak yine soft-float çağırma kurallarını kullanır (kullanın `mfloat-abi=softfp`).<br/>**Sabit**, kayan nokta yönergeleri nesil verir ve FPU'ya özgü çağırma kuralları kullanır (kullanın `mfloat-abi=hard`).|
|**ForcedIncludeFiles**|İsteğe bağlı **string []** parametresi.<br/><br/>bir veya daha çok zorunlu dosyaları içerir.<br/><br/>Kullanım `-include [name]`.|
|**FunctionLevelLinking**|İsteğe bağlı **bool** parametresi.<br/><br/>Derleyicinin ayrı ayrı işlevleri paketlenmiş işlevler (Comdat'lar) biçiminde sağlar. Düzenleme için gereken ve çalışmaya devam edin.<br/><br/>Kullanım `ffunction-sections`.|
|**GccToolChain**|İsteğe bağlı **dize** parametresi.<br/><br/>Gcc araç Zinciri'ne yönelik klasör yolu.|
|**GNUMode**|İsteğe bağlı **bool** parametresi.<br/><br/>|
|**MSCompatibility**|İsteğe bağlı **bool** parametresi.<br/><br/>Tam Microsoft Visual C++ uyumluluğu sağlayın.|
|**MSCompatibilityVersion**|İsteğe bağlı **dize** parametresi.<br/><br/>_MSC_VER içinde raporlanacak Microsoft derleyici sürümü numarasını gösteren noktayla ayrılmış değer (0 = (varsayılan)).|
|**MSExtensions**|İsteğe bağlı **bool** parametresi.<br/><br/>Microsoft derleyicisi tarafından desteklenen bazı standart dışı yapıları kabul edin.|
|**MSCompilerVersion**|İsteğe bağlı **dize** parametresi.<br/><br/>_MSC_VER içinde raporlanacak Microsoft derleyici sürümü numarasını (0 = (varsayılan)).|
|**MSVCErrorReport**|İsteğe bağlı **bool** parametresi.<br/><br/>Visual Studio dosya ve satır bilgileri için ayrıştırmak için kullanabileceğiniz hataları bildirin.|
|**ObjectFileName**|İsteğe bağlı **dize** parametresi.<br/><br/>Varsayılan nesne dosyası adını geçersiz kılacak bir ad belirtir; Dosya veya dizin adı olabilir.<br/><br/>Kullanım `/Fo[name]`.|
|**OmitFramePointers**|İsteğe bağlı **bool** parametresi.<br/><br/>Çağrı yığınında çerçeve işaretçilerinin oluşturulmasını engeller.|
|**En iyi duruma getirme**|İsteğe bağlı **dize** parametresi.<br/><br/>Uygulama için iyileştirme düzeyini belirtir.<br/><br/>**Özel**, özel iyileştirme.<br/>**Devre dışı bırakılmış**, iyileştirmeyi devre dışı bırak (kullanın `O0`).<br/>**MinSize**, boyut için İyileştir (kullanın `Os`).<br/>**MaxSpeed**, hız için İyileştir (kullanın `O2`).<br/>**Tam**, pahalı iyileştirmeler (kullanın `O3`).|
|**PositionIndependentCode**|İsteğe bağlı **bool** parametresi.<br/><br/>Paylaşılan bir kitaplık kullanmak için konum bağımsız kod (PIC) oluştur.|
|**PrecompiledHeader**|İsteğe bağlı **dize** parametresi.<br/><br/>Oluşturmayı veya kullanmayı etkinleştirir, derleme sırasında önceden derlenmiş üstbilgi.|
|**PrecompiledHeaderFile**|İsteğe bağlı **dize** parametresi.<br/><br/>Önceden derlenmiş üst bilgi dosyası için kullanılacak üst bilgi dosyası adını belirtir. Bu dosya ayrıca eklenecek **zorunlu ekleme dosyaları** derleme sırasında.|
|**PrecompiledHeaderOutputFileDirectory**|İsteğe bağlı **dize** parametresi.<br/><br/>Oluşturulan önceden derlenmiş üst bilgi dizinini belirtir. Bu dizin için de eklenecek **ek içerik dizinleri** derleme sırasında.|
|**PrecompiledHeaderCompileAs**|İsteğe bağlı **dize** parametresi.<br/><br/>Önceden derlenmiş üst bilgi dosyası için derleme dili tercihini seçin.<br/><br/>Kullanım `-x c-header`, `-x c++-header`.|
|**PreprocessorDefinitions**|İsteğe bağlı **string []** parametresi.<br/><br/>Kaynak dosyanız için ön işleme sembollerini tanımlar.<br/><br/>Kullanım `-D`.|
|**RuntimeLibrary**|İsteğe bağlı **dize** parametresi.<br/><br/>Bağlama işlemi için çalışma zamanı kitaplığını belirtin.<br/><br/>Kullanım `MSVC /MT`, `/MTd`, `/MD`, `/MDd` anahtarlar.<br/><br/>**Çok iş parçacıklı**, uygulamanızın çalışma zamanı kitaplığı çoklu iş parçacığı, statik sürümünü kullanmasını sağlar.<br/>**MultiThreadedDebug**, _DEBUG ve _MT tanımlar. Bu seçenek, aynı zamanda, derleyicinin LIBCMTD.lib kitaplık adını .obj dosyasına koyarak bağlayıcının dış simgeleri çözme sırasında LIBCMTD.lib kullanmasını sağlar.<br/>**MultiThreadedDLL**, çoklu iş parçacıklı ve DLL'ye özgü çalışma zamanı kitaplık sürümünü kullanmak için uygulamanızı neden olur. _MT ve _DLL tanımlar ve derleyicinin MSVCRT.lib kitaplık adını .obj dosyasına yerleştirmesini yerleştirin.<br/>**MultiThreadedDebugDLL**_DEBUG, _MT ve _DLL tanımlar ve uygulamanızı hata ayıklama çoklu iş parçacıklı ve DLL'ye özgü çalışma zamanı kitaplık sürümünü kullanacak şekilde neden olur. Ayrıca, derleyicinin MSVCRTD.lib kitaplık adını .obj dosyasına yerleştirmesini sağlar.|
|**RuntimeTypeInfo**|İsteğe bağlı **bool** parametresi.<br/><br/>Çalışma zamanında (çalışma zamanı tür bilgisi) C++ nesne türlerini denetlemek için kod ekler.<br/><br/>Kullanım `frtti`, `fno-rtti`.|
|**Showıncludes**|İsteğe bağlı **bool** parametresi.<br/><br/>Derleyici çıkışıyla ekleme kodu dosyalarının bir listesini oluşturur.<br/><br/>Kullanım `-H`.|
|**Kaynakları**|Gerekli **Itaskıtem []** parametresi.|
|**StrictAliasing**|İsteğe bağlı **bool** parametresi.<br/><br/>En katı örtüşme kurallarını varsayın. Bir türde bir nesne hiçbir zaman farklı türde bir nesne olarak aynı adreste bulunan olduğu kabul edilir.|
|**Sysroot**|İsteğe bağlı **dize** parametresi.<br/><br/>Üst bilgiler ve kitaplıklar için kök dizinine klasör yolu.|
|**TargetArch**|İsteğe bağlı **dize** parametresi.<br/><br/>Hedef mimari.|
|**ThumbMode**|İsteğe bağlı **dize** parametresi.<br/><br/>Thumb mikro mimarisi için yürütülen kodu oluşturur. Bu, yalnızca arm mimarisi için geçerlidir.<br/><br/>**Thumb**, Thumb kodu oluştur (kullanın `mthumb`).<br/>**ARM**, Arm kodu oluştur (kullanın `marm`).<br/>**Devre dışı bırakılmış**, seçenek seçilen platform için geçerli değil.|
|**TrackerLogDirectory**|İsteğe bağlı **dize** parametresi.<br/><br/>İzleme günlüğü dizini.|
|**TreatWarningAsError**|İsteğe bağlı **bool** parametresi.<br/><br/>Tüm Derleyici uyarılarını hata olarak değerlendirir.<br/><br/>Yeni bir proje için en iyi yöntem olabilir `/WX` tüm derlemelerde; tüm uyarıların çözümlenmesi en az sayıda olası bulunur zor kod kusurlarını sağlayacaktır.|
|**UndefinePreprocessorDefinitions**|İsteğe bağlı **string []** parametresi.<br/><br/>Bir veya daha çok önişlemci tanımsızı belirtir.<br/><br/>Kullanım `-U [macro]`.|
|**UndefineAllPreprocessorDefinitions**|İsteğe bağlı **bool** parametresi.<br/><br/>Önceden tanımlanmış tüm önişlemci değerlerini Kaldır.<br/><br/>Kullanım `-undef`.|
|**UseMultiToolTask**|İsteğe bağlı **bool** parametresi.<br/><br/>Çok işlemci derlemesi.|
|**UseShortEnums**|İsteğe bağlı **bool** parametresi.<br/><br/>Sabit listesi türünü kullanan yalnızca giriş muhtemel değerler kümesini gerektirdiği sayıda bayt.|
|**ayrıntılı**|İsteğe bağlı **bool** parametresi.<br/><br/>Ayrıntılı çıkış kullan ve çalıştırma komutları göster.|
|**WarningLevel**|İsteğe bağlı **dize** parametresi.<br/><br/>Nasıl katı derleyicinin kod hataları hakkında olmasını istediğinizi seçin. Diğer bayraklar doğrudan eklenmesi gereken **ek seçenekler** (se `/w`, `/Weverything`).<br/><br/>**TurnOffAllWarnings**, tüm Derleyici uyarılarını devre dışı bırakır (kullanın `w`).<br/>**EnableAllWarnings**, varsayılan olarak devre dışı dahil olmak üzere tüm uyarıları etkinleştirir (kullanın `Wall`).|

## <a name="see-also"></a>Ayrıca bkz.

[Görev başvurusu](../msbuild/msbuild-task-reference.md)