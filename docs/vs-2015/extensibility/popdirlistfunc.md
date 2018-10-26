---
title: POPDIRLISTFUNC | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- POPLISTFUNC
helpviewer_keywords:
- POPDIRLISTFUNC callback function
ms.assetid: 0ee90fd2-5467-4154-ab4c-7eb02ac3a14c
caps.latest.revision: 15
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4afd84af0ab6d7f801c486dd506ca5d5a10f6909
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49867968"
---
# <a name="popdirlistfunc"></a>POPDIRLISTFUNC
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu, verilen bir geri çağırma işlevini [SccPopulateDirList](../extensibility/sccpopulatedirlist-function.md) işleviyle dizinleri ve (isteğe bağlı olarak), kaynak denetimi altında olduğunu öğrenmek için dosya adları topluluğu.  
  
 `POPDIRLISTFUNC` Yalnızca dizin ve dosya adları için geri çağırma'nin çağrılabilir (verilen listedeki `SccPopulateDirList` işlevi) olan gerçekten kaynak denetimi altında.  
  
## <a name="signature"></a>İmza  
  
```cpp#  
typedef BOOL (*POPDIRLISTFUNC)(  
   LPVOID pvCallerData,  
   BOOL bFolder,  
   LPCSTR lpDirectoryOrFileName  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 pvCallerData  
 [in] Verilen kullanıcı değeri [SccPopulateDirList](../extensibility/sccpopulatedirlist-function.md).  
  
 bKlasör  
 [in] `TRUE` varsa adın `lpDirectoryOrFileName` bir dizin; Aksi takdirde adı bir dosya adıdır.  
  
 lpDirectoryOrFileName  
 [in] Kaynak kodu denetimi altında dizin veya dosya adı tam yerel yolu.  
  
## <a name="return-value"></a>Dönüş Değeri  
 IDE uygun hata kodu döndürür:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|İşleme devam edin.|  
|SCC_I_OPERATIONCANCELED|İşlemeyi durdur.|  
|SCC_E_xxx|Herhangi bir uygun kaynak denetimi hata işleme durdurmanız gerekir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa `fOptions` parametresinin `SccPopulateDirList` işlevi içeren `SCC_PDL_INCLUDEFILES` liste büyük bir olasılıkla dosya adları ve bunun yanı sıra dizin adları içerir bayrağı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDE tarafından uygulanan geri çağırma işlevleri](../extensibility/callback-functions-implemented-by-the-ide.md)   
 [SccPopulateDirList](../extensibility/sccpopulatedirlist-function.md)   
 [Hata Kodları](../extensibility/error-codes.md)

