---
title: IDebugProgram2::GetEngineInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::GetEngineInfo
helpviewer_keywords:
- IDebugProgram2::GetEngineInfo
ms.assetid: 3a4f2dc0-e082-4d8d-aeaf-463ab09d279b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: dced7f5ab415518e7f4d60c9a4555a1e89f4e770
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54937879"
---
# <a name="idebugprogram2getengineinfo"></a>IDebugProgram2::GetEngineInfo
Bu programı çalıştırmayı hata ayıklama altyapısı (DE) GUID ve adını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetEngineInfo(   
   BSTR* pbstrEngine,  
   GUID* pguidEngine  
);  
```  
  
```csharp  
int GetEngineInfo(   
   out string pbstrEngine,  
   out GUID   pguidEngine  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrEngine`  
 [out] Bu programı çalıştırmayı DE adını döndürür.  
  
 `pguidEngine`  
 [out] Bu programı çalıştırmayı DE GUİD'sini döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Her DE kendi kimlik GUİD'i tanımlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)