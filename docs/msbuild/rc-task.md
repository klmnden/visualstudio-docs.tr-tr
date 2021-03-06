---
title: RC görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- VC.Project.VCResourceCompilerTool.UndefineProcessorDefinitions
- vc.task.rc
- VC.Project.VCResourceCompilerTool.SuppressStartupBanner
- VC.Project.VCResourceCompilerTool.NullTerminateStrings
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- RC task (MSBuild (Visual C++))
- MSBuild (Visual C++), RC task
ms.assetid: 2fd26c75-a056-4dda-9f7e-2f90d3748d88
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a69649a7babacb0fe08b483380214f17f2e582f8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62974663"
---
# <a name="rc-task"></a>RC görevi
Microsoft Windows Kaynak Derleyicisi aracı sarmalar *rc.exe*. **RC** görev derler imleçler, simgeler, bit eşlemler, iletişim kutuları ve yazı tipleri gibi kaynakları bir kaynağa (*.res*) dosyası. Daha fazla bilgi için [kaynak derleyici](https://docs.microsoft.com/windows/desktop/menurc/resource-compiler).

## <a name="parameters"></a>Parametreler
 RC görevi parametreleri aşağıdaki tabloda açıklanmaktadır. Çoğu görev parametreleri ve parametrelerin birkaç kümeleri bir komut satırı seçeneğine karşılık gelir.

|Parametre|Açıklama|
|---------------|-----------------|
|**AdditionalIncludeDirectories**|İsteğe bağlı **String []** parametresi.<br /><br /> Bir dizin dahil etme dosyaları için Aranan dizinleri listesine ekler.<br /><br /> Daha fazla bilgi için **/I** seçeneğini [RC kullanma (RC komut satırı)](http://go.microsoft.com/fwlink/?LinkId=155730).|
|**AdditionalOptions**|İsteğe bağlı **dize** parametresi.<br /><br /> Komut satırı seçeneklerinin listesi; Örneğin, /\<Seçenek1 > /\<Seçenek2 > /\<seçeneği #>. Diğer tarafından temsil edilmez komut satırı seçeneklerini belirtmek için bu parametreyi kullanın **RC** görev parametresi.<br /><br /> Daha fazla bilgi için bkz. seçenekleri [RC kullanma (RC komut satırı)](http://go.microsoft.com/fwlink/?LinkId=155730).|
|**Kültür**|İsteğe bağlı **dize** parametresi.<br /><br /> Kaynaklarda kullanılan kültürü temsil eden bir yerel ayar Kimliğini belirtir.<br /><br /> Daha fazla bilgi için **/l** seçeneğini [RC kullanma (RC komut satırı)](http://go.microsoft.com/fwlink/?LinkId=155730).|
|**IgnoreStandardIncludePath**|İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true`, kaynak derleyicisi, üst bilgi veya kaynak dosyalar için aradığında, INCLUDE ortam değişkeni iade etmesini engeller.<br /><br /> Daha fazla bilgi için **/x** seçeneğini [RC kullanma (RC komut satırı)](http://go.microsoft.com/fwlink/?LinkId=155730).|
|**NullTerminateStrings**|İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true`, tüm dizeler dize tablosu boş sonlandırır.<br /><br /> Daha fazla bilgi için **/n** seçeneğini [RC kullanma (RC komut satırı)](http://go.microsoft.com/fwlink/?LinkId=155730).|
|**PreprocessorDefinitions**|İsteğe bağlı **String []** parametresi.<br /><br /> Kaynak derleyicisi için bir veya daha çok önişlemci sembolleri tanımlayın. Makro sembolleri bir listesini belirtin.<br /><br /> Daha fazla bilgi için **/d** seçeneğini [RC kullanma (RC komut satırı)](http://go.microsoft.com/fwlink/?LinkId=155730). Ayrıca bkz: **UndefinePreprocessorDefinitions** bu tablodaki.|
|**ResourceOutputFileName**|İsteğe bağlı **dize** parametresi.<br /><br /> Kaynak dosyasının adını belirtir. Bir kaynak dosya adı belirtin.<br /><br /> Daha fazla bilgi için **/fo** seçeneğini [RC kullanma (RC komut satırı)](http://go.microsoft.com/fwlink/?LinkId=155730).|
|**ShowProgress**|İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true`, derleyici, ilerleme üzerinde rapor iletilerini görüntüler.<br /><br /> Daha fazla bilgi için **/v** seçeneğini [RC kullanma (RC komut satırı)](http://go.microsoft.com/fwlink/?LinkId=155730).|
|**Kaynak**|Gerekli `ITaskItem[]` parametresi.<br /><br /> Tüketilen ve görevler tarafından yayılan MSBuild kaynak dosya öğeleri bir dizisi tanımlanmaktadır.|
|**SuppressStartupBanner**|İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true`, görev başladığında telif hakkı ve sürüm numarası iletisinin görüntülenmesini engeller.<br /><br /> Daha fazla bilgi için **/?** komut satırı seçeneğini ve ardından bakın **/nologo** seçeneği.|
|**TrackerLogDirectory**|İsteğe bağlı **dize** parametresi.<br /><br /> İzleme günlüğü dizini belirtir.|
|**UndefinePreprocessorDefinitions**|Önişlemci simge tanımlarını Kaldır.<br /><br /> Daha fazla bilgi için **/u** seçeneğini [RC kullanma (RC komut satırı)](http://go.microsoft.com/fwlink/?LinkId=155730). Ayrıca bkz: **PreprocessorDefinitions** bu tablodaki.|

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)