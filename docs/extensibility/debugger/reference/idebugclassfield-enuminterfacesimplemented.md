---
title: IDebugClassField::EnumInterfacesImplemented | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugClassField::EnumInterfacesImplemented
helpviewer_keywords:
- IDebugClassField::EnumInterfacesImplemented method
ms.assetid: e5523e45-d350-491e-a92c-fe0ca97d2052
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: da72bcbe32a4de2760d7b42a580c0550b5cfa17f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54944741"
---
# <a name="idebugclassfieldenuminterfacesimplemented"></a>IDebugClassField::EnumInterfacesImplemented
Bu sınıf tarafından uygulanan arabirimler için bir numaralandırıcı oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumInterfacesImplemented(   
   IEnumDebugFields** ppEnum  
);  
```  
  
```csharp  
int EnumInterfacesImplemented(  
   out IEnumDebugFields ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) uygulanan arabirimlerin listesini temsil eden nesne. Arabirimlerine yoksa null değeri döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür veya bu sınıfa uygulanan arabirim varsa S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Her öğenin sabit bir [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) bir arabirim tanımlayan nesne. Yönetilmeyen Not [!INCLUDE[vcprvc](../../../code-quality/includes/vcprvc_md.md)] kod bu yöntem her zaman için yönetilmeyen bir null değer döndürecek şekilde ayrık bir varlık olarak arabirimleri kullanmayan [!INCLUDE[vcprvc](../../../code-quality/includes/vcprvc_md.md)] kod.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)   
 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)