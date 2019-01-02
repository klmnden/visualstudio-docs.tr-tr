---
title: IDebugModuleLoadEvent2::GetModule | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugModuleLoadEvent2::GetModule
helpviewer_keywords:
- IDebugModuleLoadEvent2::GetModule
ms.assetid: c86482bb-9ce5-4e63-bbe0-969b50169424
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f1b9170db806ac4b501d6acf7ad66f90be6aea75
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53892867"
---
# <a name="idebugmoduleloadevent2getmodule"></a>IDebugModuleLoadEvent2::GetModule
Yüklenmekte olan modül alır yüklü veya kaldırılmış.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetModule(   
   IDebugModule2** pModule,  
   BSTR*           pbstrDebugMessage,  
   BOOL*           pbLoad  
);  
```  
  
```csharp  
int GetModule(   
   out IDebugModule2 pModule,  
   ref string        pbstrDebugMessage,  
   ref int           pbLoad  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pModule`  
 [out] Döndürür bir [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md) yüklenmesi veya kaldırılması modülü temsil eden nesne.  
  
 `pbstrDebugMessage`  
 [out içinde] Bu olay açıklayan isteğe bağlı bir ileti döndürür. Bu parametre null değeri ise, hiçbir ileti istenir.  
  
 `pbLoad`  
 [out içinde] Sıfır olmayan (`TRUE`) Modül yükleme ve sıfır ise (`FALSE`) modülü kaldırma durumunda. Bu parametre null değeri ise, hiçbir durum istenir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugModuleLoadEvent2](../../../extensibility/debugger/reference/idebugmoduleloadevent2.md)   
 [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)