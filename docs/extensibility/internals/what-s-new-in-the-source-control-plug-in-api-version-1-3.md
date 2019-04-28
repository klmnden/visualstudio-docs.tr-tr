---
title: Hangi&#39;da kaynak denetimi eklentisi API sürümü 1.3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, what's new in API v1.3
- what's new [Visual Studio SDK], source control plug-ins
ms.assetid: 7dfb2227-6e1d-4028-bce9-f8967456a993
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8b61e56fcef8bbbe8e9f36a39580eae14ad582d5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62856714"
---
# <a name="what39s-new-in-the-source-control-plug-in-api-version-13"></a>Hangi&#39;da kaynak denetimi eklentisi API sürümü 1.3
Kaynak Denetimi Eklentisi API sürümü 1.3 daha gelişmiş bir denetim sağlamak için aşağıdaki yeni işlevler sunar.

## <a name="changes"></a>Değişiklikler
 Aşağıdaki işlevleri, kaynak denetimi eklentisi API sürümü 1.3 için yenidir:

|İşlev|Genel Bakış|
|--------------|--------------|
|[SccGetExtendedCapabilities](../../extensibility/sccgetextendedcapabilities-function.md)|Ek özellik BITS bildirilmesini sağlar.|
|[SccEnumChangedFiles](../../extensibility/sccenumchangedfiles-function.md)|Sürüm denetimi veritabanı yerel diskteki yeni sürümlere sahip dosyalar incelenmesi sağlar|
|[SccQueryChanges](../../extensibility/sccquerychanges-function.md)|Ad değişiklikleri (yeniden adlandırma, ekleme ve silme işlemleri) durumunu incelenmesi için belirtilen dosyaları sağlar.|
|[SccPopulateDirList](../../extensibility/sccpopulatedirlist-function.md)|Dizinleri ve dosyaları incelenmesi sürüm denetim veritabanındaki sağlar|
|[SccAddFilesFromSCC](../../extensibility/sccaddfilesfromscc-function.md)|Belirtilen dosyaların listesini sürüm denetim veritabanından geçerli projeye ekler.|
|[SccBackgroundGet](../../extensibility/sccbackgroundget-function.md)|Sessiz "Al" (kullanıcı arabirimi gösterilir) belirtilen dosyaları gerçekleştirir|
|[SccGetUserOption](../../extensibility/sccgetuseroption-function.md)|Kullanıcıya özgü seçenekleri erişmesini sağlar|

## <a name="see-also"></a>Ayrıca Bkz.
- [Başlarken](../../extensibility/internals/getting-started-with-source-control-plug-ins.md)
- [Kaynak Denetimi Eklentisi API Sürümü 1.2’deki Yenilikler](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)