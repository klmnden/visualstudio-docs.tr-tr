---
title: Hangi&#39;da kaynak denetimi eklentisi API sürümü 1.3 | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- source control plug-ins, what's new in API v1.3
- what's new [Visual Studio SDK], source control plug-ins
ms.assetid: 7dfb2227-6e1d-4028-bce9-f8967456a993
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f6abe06f57e0e7ba83298f8dd5b2658a8f2e26c1
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49242118"
---
# <a name="what39s-new-in-the-source-control-plug-in-api-version-13"></a>Hangi&#39;da kaynak denetimi eklentisi API sürümü 1.3
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

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
 [Çalışmaya başlama](../../extensibility/internals/getting-started-with-source-control-plug-ins.md)   
 [Kaynak Denetimi Eklentisi API Sürümü 1.2’deki Yenilikler](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)

