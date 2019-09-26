---
title: Tasarım zamanında derlemeleri çözme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- msbuild
ms.assetid: 20dae076-733e-49c1-a2e9-b336757ae21d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 131cc61614c9f3e814cca5bcbc0ff6db303414cf
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253751"
---
# <a name="resolve-assemblies-at-design-time"></a>Tasarım zamanında derlemeleri çözümleyin
Başvuru **Ekle** iletişim kutusunun **.net** sekmesi aracılığıyla bir derlemeye başvuru eklediğinizde, başvuru bir ara başvuru derlemesine işaret eder; diğer bir deyişle, tüm tür ve imza bilgilerini içeren, ancak herhangi bir kod içermesi gerekmeyen bir derlemedir. **.Net** sekmesi .NET Framework çalışma zamanı derlemelerine karşılık gelen başvuru derlemelerini listeler. Ayrıca, üçüncü taraflar tarafından kullanılan kayıtlı AssemblyFoldersEx klasörlerindeki çalışma zamanı derlemelerine karşılık gelen başvuru derlemelerini listeler.

## <a name="multi-targeting"></a>Çoklu hedefleme
 [!INCLUDE[vs_dev12](../extensibility/includes/vs_dev12_md.md)], ortak dil çalışma zamanı (CLR) sürüm 2,0 veya sürüm 4 ' te çalıştırılan .NET Framework sürümlerini hedeflemenizi sağlar. Bu sürümler 2,0, 3,0, 3,5, 4, 4,5, ve 4.5.1 sürümlerini ve Silverlight sürümlerini 1,0, 2,0 ve 3,0 içerir .NET Framework. CLR sürüm 2,0 veya sürüm 4 ' ü temel alan yeni bir .NET Framework sürümü yayınlanmışsa, Framework bir hedefleme paketi kullanılarak yüklenebilir ve Visual Studio 'da otomatik olarak bir hedef olarak görünür.

## <a name="how-type-resolution-works"></a>Tür çözümlemenin çalışması
 Çalışma zamanında, CLR GAC 'ye, *bin* dizinine ve herhangi bir yoklama yoluna bakarak derlemedeki türleri çözümler. Bu, Fusion yükleyicisi tarafından işlenir. Ancak, Fusion yükleyici ne aradıklarını nasıl bilir? Bu, uygulama yapılandırıldığında tasarım zamanında yapılan bir çözüme bağlıdır.

 Derleme sırasında derleyici, başvuru derlemelerini kullanarak uygulama türlerini çözümler. .NET Framework sürümleri 2,0, 3,0, 3,5, 4, 4,5 ve 4.5.1 sürümlerinde, .NET Framework yüklendiğinde başvuru derlemeleri yüklenir.

 Başvuru derlemeleri, .NET Framework SDK 'nın ilgili sürümüyle birlikte gelen hedefleme paketi tarafından sağlanır. Framework yalnızca çalışma zamanı derlemelerini sağlar. Uygulama derlemek için hem .NET Framework hem de karşılık gelen .NET Framework SDK 'sını yüklemeniz gerekir.

 Belirli bir .NET Framework hedeflediğinizde, yapı sistemi hedefleme paketindeki başvuru derlemelerini kullanarak tüm türleri çözümler. Çalışma zamanında Fusion yükleyici, genellikle GAC 'de bulunan çalışma zamanı Derlemeleriyle aynı türleri çözümler.

 Başvuru derlemeleri kullanılamıyorsa, derleme sistemi, derleme türlerini çalışma zamanı derlemelerini kullanarak çözer. GAC 'deki çalışma zamanı derlemeleri alt sürüm numaralarına göre ayırt olmadığından, yanlış derlemeye çözümlemenin yapılması mümkündür. Bu durum örneğin, 3,5 sürümü ' de sunulan yeni bir yönteme, sürüm 3,0 .NET Framework ' i hedeflerken başvuruluyorsa meydana gelebilir. Yapı başarılı olur ve uygulama derleme makinesinde çalışır, ancak sürüm 3,5 yüklü olmayan bir makineye dağıtıldığında başarısız olur.

 Artık .NET Framework SDK ile birlikte sunulan hedefleme paketi, bu çerçevenin bu sürümündeki çalışma zamanı derlemelerinin tümünün bir listesini içerir, yeniden dağıtım (Redist) listesi denir ve derleme sisteminin, türleri yanlış bir şekilde çözümlemesini olanaksız hale getirir derlemenin sürümü.

## <a name="see-also"></a>Ayrıca bkz.
- [Gelişmiş kavramlar](../msbuild/msbuild-advanced-concepts.md)