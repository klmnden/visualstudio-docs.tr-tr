---
title: Hedefleri ve görevleri yapılandırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 9aabe67a-1720-4bbf-80d3-822b3ccf75c0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: de6f1168b55af2337dfb235d05c9c8376b2614c1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62778253"
---
# <a name="configure-targets-and-tasks"></a>Hedefleri ve görevleri yapılandırma
MSBuild hedefleri ve görevleri çalıştırmak için yapılandırabilirsiniz giden işlem MSBuild ile böylece üzerinde çalıştığını olandan farklı Bağlamlar hedefleyebilirsiniz. Örneğin, geliştirme bilgisayarında .NET Framework 4.5 64-bit işletim sisteminde çalışırken bir 32 bitlik .NET Framework 2.0 uygulama hedefleyebilirsiniz. .NET Framework 4 veya önceki sürümleri çalıştıran bilgisayarlar ayrıca hedefleyebilirsiniz. 32 veya 64 bit ve belirli bir .NET Framework sürüm birleşimi olarak da bilinen *hedef bağlam*.

## <a name="installation"></a>Yükleme
 .NET Framework 4.5 ve 4.5.1 yeniden adlandırma olmadan ortak dil çalışma zamanı (CLR), hedefler, görevleri ve araçlar .NET Framework 4'ün değiştirin. .NET Framework 4.5.1 parçası olarak yüklü [!INCLUDE[vs_dev12](../extensibility/includes/vs_dev12_md.md)].

 MSBuild Visual Studio'dan ayrı olarak yüklemek istiyorsanız, yükleme paketinden indirebilirsiniz [MSBuild indirme](http://go.microsoft.com/fwlink/?LinkId=309745). Ayrıca, kullanmak istediğiniz .NET Framework sürümleri yüklemeniz gerekir.

## <a name="targets-and-tasks"></a>Hedefleri ve görevleri
 MSBuild çalıştırmaları belirli bağlamları daha büyük bir hedef için işlem dışı Görevler oluşturun.  Örneğin, 32-bit MSBuild 64 bit bilgisayar hedeflemek için 64-bit işlem içinde derleme görevi çalışabilir. Bu tarafından denetlenir `UsingTask` bağımsız değişkenleri ve `Task` parametreleri. Bu bağımsız değişkenleri ve parametreleri tarafından .NET Framework 4.5 yüklü hedeflerini ayarlayın ve değişiklik çeşitli hedef bağlamları yönelik uygulamalar oluşturmak için gerekli değildir.

 Kendi hedef bağlam oluşturmak istiyorsanız, bu bağımsız değişkenleri ve parametreleri uygun şekilde ayarlamanız gerekir. .NET Framework 4.5 içinde Ara *Microsoft.Common.targets* dosya ve *Microsoft.Common.Tasks* örnekler için dosya.  Birden fazla hedef bağlamı ile çalışabilmeniz için özel bir görev oluşturma veya var olan görevleri değişiklik yapma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Hedefleri ve görevleri yapılandırma](../msbuild/how-to-configure-targets-and-tasks.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Çoklu Sürüm Desteği](../msbuild/msbuild-multitargeting-overview.md)