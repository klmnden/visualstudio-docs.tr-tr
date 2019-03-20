---
title: XDCMake görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vc.task.xdcmake
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- XDCMake task (MSBuild (Visual C++))
- MSBuild (Visual C++), XDCMake task
ms.assetid: a7de9c64-903a-4a02-85f3-f37672270f25
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fa868695316ec83e066885590f859af947660625
ms.sourcegitcommit: 4d9c54f689416bf1dc4ace058919592482d02e36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "58195040"
---
# <a name="xdcmake-task"></a>XDCMake görevi
XML belgelendirme aracı sarmalar (*xdcmake.exe'yi*), XML belgesi açıklaması birleştirir (*.xdc*) dosyalarınızı bir *.xml* dosya.

 Bir *.xdc* dosyasını kullanarak Visual C++ kaynak kod ve derleme belge açıklamaları sağladığınızda oluşturulan [/doc](/cpp/build/reference/doc-process-documentation-comments-c-cpp) derleyici seçeneği. Daha fazla bilgi için [XDCMake başvurusu](/cpp/build/reference/xdcmake-reference), [XML belgesi oluşturma aracı özellik sayfaları](/cpp/build/reference/xml-document-generator-tool-property-pages)ve komut satırı Yardımı seçeneği (**/?**) için *xdcmake.exe'yi* .

## <a name="remarks"></a>Açıklamalar
 Varsayılan olarak, *xdcmake.exe'yi* araç birkaç komut satırı seçeneklerini destekler. Ek seçenekler, belirttiğiniz zaman desteklenir **/eski** komut satırı seçeneği.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır **XDCMake** görev.

|Parametre|Açıklama|
|---------------|-----------------|
|**AdditionalDocumentFile**|İsteğe bağlı **String []** parametresi.<br /><br /> Belirten bir veya daha fazla ek *.xdc* birleştirilecek dosyaları.<br /><br /> Daha fazla bilgi için **ek belge dosyaları** açıklamasında [XML belgesi oluşturma aracı özellik sayfaları](/cpp/build/reference/xml-document-generator-tool-property-pages). Ayrıca bkz: **/eski** ve **/Fs** için komut satırı seçenekleri *xdcmake.exe'yi*.|
|**AdditionalOptions**|İsteğe bağlı **dize** parametresi.<br /><br /> Komut satırında belirtilen seçeneklerin bir listesi. Örneğin, /\<Seçenek1 > /\<Seçenek2 > /\<seçeneği #>. Diğer tarafından temsil edilmez seçeneklerini belirtmek için bu parametreyi kullanın **XDCMake** görev parametresi.<br /><br /> Daha fazla bilgi için [XDCMake başvurusu](/cpp/build/reference/xdcmake-reference), [XML belgesi oluşturma aracı özellik sayfaları](/cpp/build/reference/xml-document-generator-tool-property-pages)ve komut satırı Yardımı (**/?**) için *xdcmake.exe'yi*.|
|**DocumentLibraryDependencies**|İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true` ve geçerli proje üzerinde bir statik kitaplık bağımlılığı (*.lib*) çözümde proje *.xdc* kitaplığı proje dosyaları dahil edilecek *.xml* geçerli projenin çıkış dosyası.<br /><br /> Daha fazla bilgi için **belge kitaplığı bağımlılıkları** açıklamasında [XML belgesi oluşturma aracı özellik sayfaları](/cpp/build/reference/xml-document-generator-tool-property-pages).|
|**OutputFile**|İsteğe bağlı **dize** parametresi.<br /><br /> Varsayılan çıkış dosyası adını geçersiz kılar. Varsayılan adı ilk adından türetilir *.xdc* işlenen dosya.<br /><br /> Daha fazla bilgi için **/out:\<filename >** seçeneğini [XDCMake başvurusu](/cpp/build/reference/xdcmake-reference). Ayrıca bkz: **/eski** ve **/Fo** için komut satırı seçenekleri *xdcmake.exe'yi*.|
|**projectName**|İsteğe bağlı **dize** parametresi.<br /><br /> Geçerli projenin adı.|
|**SlashOld**|İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true`, ek etkinleştirir *xdcmake.exe'yi* seçenekleri.<br /><br /> Daha fazla bilgi için **/eski** için komut satırı seçeneği *xdcmake.exe'yi*.|
|**Kaynakları**|Gerekli `ITaskItem[]` parametresi.<br /><br /> Tüketilen ve görevler tarafından yayılan MSBuild kaynak dosya öğeleri bir dizisi tanımlanmaktadır.|
|**SuppressStartupBanner**|İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true`, görev başladığında telif hakkı ve sürüm numarası iletisinin görüntülenmesini engeller.<br /><br /> Daha fazla bilgi için **/nologo** seçeneğini [XDCMake başvurusu](/cpp/build/reference/xdcmake-reference).|
|**TrackerLogDirectory**|İsteğe bağlı **dize** parametresi.<br /><br /> İzleyici günlüğü dizini belirtir.|

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)