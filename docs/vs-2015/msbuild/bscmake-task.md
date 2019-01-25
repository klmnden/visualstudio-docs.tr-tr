---
title: BscMake görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- vc.task.bscmake
- VC.Project.VCBscMakeTool.PreserveSBR
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), tasks
- BscMake task (MSBuild (Visual C++))
ms.assetid: bb98fc67-cad8-43a7-9598-60df6d734db2
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c21c14b8c84246545d9ffb3e3dc59210b56fe84e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54777158"
---
# <a name="bscmake-task"></a>BscMake Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
ÖNEMLİ]
>  bscmake artık Visual Studio IDE tarafından kullanılır. Visual Studio 2008'den itibaren gözatma bilgilerini otomatik olarak bir .sdf dosyası çözüm klasöründe depolanır.  
  
 Microsoft gözatma bilgisi bakım Yardımcısı Aracı (bscmake.exe) sarmalar.  Bscmake.exe aracı, derleme sırasında oluşturulan kaynak tarayıcı dosyaları (.sbr) öğesinden gözatma bilgisi dosyası (.bsc) oluşturur. Kullanım **Nesne Tarayıcısı** .bsc dosyasını görüntülemek için. Daha fazla bilgi için [BSCMAKE başvurusu](http://msdn.microsoft.com/library/b97ad994-1355-4809-98db-6abc12c6fb13).  
  
## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır **BscMake** görev. Çoğu görev parametreleri bir komut satırı seçeneğine karşılık gelir.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|**AdditionalOptions**|İsteğe bağlı **dize** parametresi.<br /><br /> Komut satırında belirtilen seçeneklerin bir listesi. Örneğin, "/*Seçenek1* /*Seçenek2* /*seçeneği #*". Diğer tarafından temsil edilmez seçeneklerini belirtmek için bu parametreyi kullanın **BscMake** görev parametresi.<br /><br /> Daha fazla bilgi için bkz. seçenekleri [BSCMAKE seçenekleri](http://msdn.microsoft.com/library/fa2f1e06-c684-41cf-80dd-6a554835ebd2).|  
|**OutputFile**|İsteğe bağlı **dize** parametresi.<br /><br /> Varsayılan çıkış dosyası adını geçersiz kılan bir dosya adını belirtir.<br /><br /> Daha fazla bilgi için **/o** seçeneğini [BSCMAKE seçenekleri](http://msdn.microsoft.com/library/fa2f1e06-c684-41cf-80dd-6a554835ebd2).|  
|**PreserveSBR**|İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true`, artımlı olmayan bir derleme zorlar. Tam ve artımlı olmayan bir derleme mi .bsc dosyası var ve .sbr dosyaları kesildi öğesinden engeller bağımsız olarak gerçekleşir.<br /><br /> Daha fazla bilgi için **/n** seçeneğini [BSCMAKE seçenekleri](http://msdn.microsoft.com/library/fa2f1e06-c684-41cf-80dd-6a554835ebd2).|  
|**Kaynakları**|İsteğe bağlı **Itaskıtem []** parametresi.<br /><br /> Tüketilen ve görevler tarafından yayılan MSBuild kaynak dosya öğeleri bir dizisi tanımlanmaktadır.|  
|**SuppressStartupBanner**|İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true`, görev başladığında telif hakkı ve sürüm numarası iletisinin görüntülenmesini engeller.<br /><br /> Daha fazla bilgi için **/nologo** seçeneğini [BSCMAKE seçenekleri](http://msdn.microsoft.com/library/fa2f1e06-c684-41cf-80dd-6a554835ebd2).|  
|**TrackerLogDirectory**|İsteğe bağlı **dize** parametresi.<br /><br /> İzleyici günlüğü dizini belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
