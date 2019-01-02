---
title: Dizin durumu kod numaralandırıcısı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- directory status code enumerator
- source control plug-ins, directory status enumeration
ms.assetid: 616026b5-f529-40ef-90c1-1836e116d797
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: a8d6a541415e42e8d35dc4f3ab814c89cf939beb
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53927616"
---
# <a name="directory-status-code-enumerator"></a>Dizin durumu kod numaralandırıcısı
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
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Kaynak denetimi eklentileri](../extensibility/source-control-plug-ins.md)   
 [SccDirQueryInfo](../extensibility/sccdirqueryinfo-function.md)