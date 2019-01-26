---
title: IDebugProgram2::WriteDump | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::WriteDump
helpviewer_keywords:
- IDebugProgram2::WriteDump
ms.assetid: 375afb8c-882d-44db-bfa7-e2c9eb555122
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f4fc77748e456a612130de4b8f814ea7ba491f22
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55021851"
---
# <a name="idebugprogram2writedump"></a>IDebugProgram2::WriteDump
Bir döküm bir dosyaya yazar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT WriteDump(   
   DUMPTYPE  DumpType,  
   LPCOLESTR pszDumpUrl  
);  
```  
  
```csharp  
int WriteDump(   
   enum_DUMPTYPE  DumpType,  
   string         pszDumpUrl  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `DumpType`  
 [in] Bir değer [DUMPTYPE](../../../extensibility/debugger/reference/dumptype.md) Örneğin, kısa döküm, türünü belirten sabit listesi veya uzun süre.  
  
 `pszDumpUrl`  
 [in] Döküm için yazma URL'si. Genellikle, bu biçimindedir `file://c:\path\filename.ext`, ancak geçerli bir URL olabilir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir program dökümü genellikle verilebilir geçerli yığın çerçevesi yığın, program ve program sahip büyük olasılıkla herhangi bir bellek çalışan iş parçacıkları listesi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)