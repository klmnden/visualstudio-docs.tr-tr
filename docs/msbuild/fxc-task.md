---
title: FXC görev | Microsoft Docs
ms.date: 03/10/2019
ms.topic: reference
f1_keywords:
- vc.task.fxc
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), FXC task
- FXC task (MSBuild (Visual C++))
author: mikeblome
ms.author: mblome
ms.workload:
- multiple
ms.openlocfilehash: 65819f1625477effab024055828301b26ab5804a
ms.sourcegitcommit: d78821f8c353e0102b1554719f549f32dffac71b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2019
ms.locfileid: "58515171"
---
# <a name="fxc-task"></a>FXC görevi

HLSL gölgelendirici derleyicileri, yapı işleminde kullanın.

## <a name="parameters"></a>Parametreler

Parametreleri aşağıdaki tabloda açıklanmıştır **FXC** görev.

|Parametre|Açıklama|
|---------------|-----------------|
|**AdditionalIncludeDirectories**|İsteğe bağlı **string []** parametresi.<br/><br/>Ekleme yoluna eklenecek bir veya daha fazla dizin belirtir; birden fazla ise noktalı virgülle ayırın.<br/><br/>Kullanım `/I[path]`.|
|**AdditionalOptions**|İsteğe bağlı **dize** parametresi.|
|**AllResourcesBound**|İsteğe bağlı **bool** parametresi.<br/><br/>Derleyici, gölgelendiricinin tüm kaynaklar sınırlı ve iyi durumda olduğundan gölgelendirici yürütme süresi boyunca varsayar. Gölgelendirici modeli 5.1 ve üzeri kullanılabilir.<br/><br/>Kullanım `/all_resources_bound`.|
|**AssemblerOutput**|İsteğe bağlı **dize** parametresi.<br/><br/>Assembly dili çıkış dosyasının içeriğini belirtir.<br/><br/>Kullanım `/Fc, /Fx`.<br/><br/>**NoListing**<br/>**AssemblyCode**, kullanın `Fc`.<br/>**AssemblyCodeAndHex**, kullanın `Fx`.|
|**AssemblerOutputFile**|İsteğe bağlı **dize** parametresi.<br/><br/>Derleme kodu liste dosyasının adını belirtir.|
|**CompileD2DCustomEffect**|İsteğe bağlı **bool** parametresi.<br/><br/>Piksel gölgelendiricileri içeren bir Direct2D özel efekti derleyin. Olmayan bir köşe için kullanabilir veya özel efekti.|
|**ConsumeExportFile**|İsteğe bağlı **dize** parametresi.|
|**DisableOptimizations**|İsteğe bağlı **bool** parametresi.<br/><br/>İyileştirmeleri devre dışı bırakın.<br/><br/>`/Od` gelir `/Gfp` çıkış aynı olmasa da `/Od /Gfp`.|
|**EnableDebuggingInformation**|İsteğe bağlı **bool** parametresi.<br/><br/>Hata ayıklamayı etkinleştir bilgileri.|
|**EnableUnboundedDescriptorTables**|İsteğe bağlı **bool** parametresi.<br/><br/>Derleyici, gölgelendiricinin Sınırlanmamış aralığa sahip bir kaynak dizisi bildirimi içerebileceği bildirin. Gölgelendirici modeli 5.1 ve üzeri kullanılabilir.<br/><br/>Kullanım `/enable_unbounded_descriptor_tables`.|
|**EntryPointName**|İsteğe bağlı **dize** parametresi.<br/><br/>Gölgelendirici için giriş noktası adını belirtir.<br/><br/>Kullanım `/E[name]`.|
|**GenerateExportFile**|İsteğe bağlı **dize** parametresi.|
|**GenerateExportShaderProfile**|İsteğe bağlı **dize** parametresi.|
|**HeaderFileOutput**|İsteğe bağlı **dize** parametresi.<br/><br/>Nesne kodunu içeren üst bilgi dosyasının adını belirtir.<br/><br/>Kullanım `/Fh [name]`.|
|**ObjectFileOutput**|İsteğe bağlı **dize** parametresi.<br/><br/>Nesne dosyası adını belirtir.<br/><br/>Kullanım `/Fo [name]`.|
|**PreprocessorDefinitions**|İsteğe bağlı **string []** parametresi.<br/><br/>Kaynak dosyanız için ön işleme sembollerini tanımlar.|
|**SetRootSignature**|İsteğe bağlı **dize** parametresi.<br/><br/>Gölgelendirici bytecode'una kök imzasını iliştirin. Gölgelendirici modeli 5.0 ve üzeri kullanılabilir.<br/><br/>Kullanım `/setrootsignature`.|
|**ShaderModel**|İsteğe bağlı **dize** parametresi.<br/><br/>Gölgelendirici modelini belirtir. Bazı gölgelendirici türleri yalnızca yeni gölgelendirici modelleriyle birlikte kullanılabilir.<br/><br/>Kullanım `/T [type]_[model]`.|
|**ShaderType**|İsteğe bağlı **dize** parametresi.<br/><br/>Gölgelendirici türünü belirtir.<br/><br/>Kullanım `/T [type]_[model]`.<br/><br/>**Etkili**, kullanın `fx`.<br/>**Köşe**, kullanın `vs`.<br/>**Piksel**, kullanın `ps`.<br/>**Geometri**, kullanın `gs`.<br/>**Kabuk**, kullanın `hs`.<br/>**Etki alanı**, kullanın `ds`.<br/>**İşlem**, kullanın `cs`.<br/>**Kitaplık**, kullanın `lib`.<br/>**RootSignature**, kök imza nesnesi oluştur.|
|**Kaynak**|Gerekli **Itaskıtem** parametresi.|
|**SuppressStartupBanner**|İsteğe bağlı **bool** parametresi.<br/><br/>Başlangıç başlığının ve bilgi iletilerinin görüntülenmesini bastırır.<br/><br/>Kullanım `/nologo`.|
|**TrackerLogDirectory**|İsteğe bağlı **dize** parametresi.|
|**TreatWarningAsError**|İsteğe bağlı **bool** parametresi.<br/><br/>Tüm Derleyici uyarılarını hata olarak değerlendirir.<br/><br/>Yeni bir proje için en iyi yöntem olabilir `/WX` tüm derlemelerde; tüm uyarıların çözümlenmesi en az sayıda olası bulunur zor kod kusurlarını sağlayacaktır.|
|**Değişkenadı**|İsteğe bağlı **dize** parametresi.<br/><br/>Üstbilgi dosyasında değişken adı için bir ad belirtir.<br/><br/>Kullanım `/Vn [name]`.|

## <a name="see-also"></a>Ayrıca bkz.

[Görev başvurusu](../msbuild/msbuild-task-reference.md)