---
title: Idiareadexeatrvacallback::readexecutableatrva | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaReadExeAtRVACallback::ReadExecutableAtRVA method
ms.assetid: 3c1e965f-8f05-41a8-86d8-01830b2377c9
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 42f61d7e844038812175032ab9b8caaa90b088ec
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49868215"
---
# <a name="idiareadexeatrvacallbackreadexecutableatrva"></a>IDiaReadExeAtRVACallback::ReadExecutableAtRVA
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bayt belirtilen göreli sanal adres (RVA) yürütülebilir dosyasından başlayarak belirtilen sayıda okur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT ReadExecutableAtRVA (   
   DWORD  relativeVirtualAddress,  
   DWORD  cbData,  
   DWORD* pcbData,  
   BYTE   data[]  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `relativeVirtualAddress`  
 [in] Okumanın başlatılacağı RVA yürütülebilir dosya.  
  
 `cbData`  
 [in] Okunacak bayt sayısı.  
  
 `pcbData`  
 [out] Okunan bayt sayısını döndürür.  
  
 `data[]`  
 [out içinde] Dosyadan okunan bayt ile doldurulmuş bir dizi.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bir göreli sanal adres kullanarak bir çalıştırılabilir dosyadan veri baytı yüklenecek DIA destek kod tarafından çağrılır. Support, bu yöntem çağrılır [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiareadexeatrvacallback](../../debugger/debug-interface-access/idiareadexeatrvacallback.md)   
 [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)



