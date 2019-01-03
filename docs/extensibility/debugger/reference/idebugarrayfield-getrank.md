---
title: IDebugArrayField::GetRank | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugArrayField::GetRank
helpviewer_keywords:
- IDebugArrayField::GetRank method
ms.assetid: 2364b876-5be1-4bab-9b8f-3b6121da35c6
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: daf4a0ebf22e66629faa97706eeef033642f03b0
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53985296"
---
# <a name="idebugarrayfieldgetrank"></a>IDebugArrayField::GetRank
Derece veya dizinin boyut sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetRank(   
   DWORD* pdwRank  
);  
```  
  
```csharp  
int GetRank(  
   out uint pdwRank  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pdwRank`  
 [out] Derecesini döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Boyut sayısı bir dizi boyut sayısını karşılık gelir. C++ ve C#, çok boyutlu diziler dizilerdir dizilerinin gerçekten ve bu nedenle yalnızca tek boyutlu bir dizi olarak düşünülebilir (ve `GetRank` yöntemi her zaman 1 döndüren). İçinde [!INCLUDE[vbprvb](../../../code-quality/includes/vbprvb_md.md)], diğer taraftan, çok boyutlu diziler farklı şekilde işlenir ve boyut sayısı gibi bir dizi boyut sayısını yansıtır (ve `GetRank` yöntemi her zaman bir boyut sayısını döndürür).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugArrayField](../../../extensibility/debugger/reference/idebugarrayfield.md)