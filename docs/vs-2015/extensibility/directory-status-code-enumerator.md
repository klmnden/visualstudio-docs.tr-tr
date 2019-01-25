---
title: Dizin durumu kod numaralandırıcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- directory status code enumerator
- source control plug-ins, directory status enumeration
ms.assetid: 616026b5-f529-40ef-90c1-1836e116d797
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: e082a691a389d5cb9a8fa307a627b11911e0db78
ms.sourcegitcommit: c496a77add807ba4a29ee6a424b44a5de89025ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54834521"
---
# <a name="directory-status-code-enumerator"></a>Dizin Durumu Kod Numaralandırıcısı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

`SccDirStatus` Numaralandırıcı kaynak denetimi Sistemi'nde bir dizin durumunu belirten adlandırılmış sabit değerleri içerir. Bu sabit listesi tarafından kullanılan [Sccdirqueryınfo](../extensibility/sccdirqueryinfo-function.md). Bu kaynak denetimi eklentisi API 1.2 sürümünde kullanıma sunulmuştur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
enum SccDirStatus {  
   SCC_DIRSTATUS_INVALID       = -1L,  
   SCC_DIRSTATUS_NOTCONTROLLED = 0x0000L,  
   SCC_DIRSTATUS_CONTROLLED    = 0x0001L,  
   SCC_DIRSTATUS_EMPTYPROJ     = 0x0002L  
};  
```  
  
## <a name="members"></a>Üyeler  
 SCC_DIRSTATUS_INVALID  
 Durumu alınamadı; üzerinde güvenmeyin.  
  
 SCC_DIRSTATUS_NOTCONTROLLED  
 Dizin, kaynak denetimi altında değil.  
  
 SCC_DIRSTATUS_CONTROLLED  
 Kaynak denetimi altında dizindir.  
  
 SCC_DIRSTATUS_EMPTYPROJ  
 Bu dizine karşılık gelen proje boştur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak denetimi eklentileri](../extensibility/source-control-plug-ins.md)   
 [SccDirQueryInfo](../extensibility/sccdirqueryinfo-function.md)
