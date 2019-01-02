---
title: Idiaenumınjectedsources::get_Count | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumInjectedSources::get_Count method
ms.assetid: 659c415b-9f7b-470d-90e2-b4c0087f8dd3
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 07bc92debfeffc4973a160dd0f31a89e746b976e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53867322"
---
# <a name="idiaenuminjectedsourcesgetcount"></a>IDiaEnumInjectedSources::get_Count
Eklenen kaynağı sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_Count (   
   LONG* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pRetVal  
 [out] Eklenen kaynağı sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumınjectedsources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)   
 [IDiaEnumInjectedSources::Item](../../debugger/debug-interface-access/idiaenuminjectedsources-item.md)