---
title: IDebugClassField::EnumConstructors | Microsoft Docs
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
- IDebugClassField::EnumConstructors
helpviewer_keywords:
- IDebugClassField::EnumConstructors method
ms.assetid: 66a250b2-75a0-45aa-8d58-40f91cc4bf7b
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 526e0b129e07a7c52f7f4215e1f61d1c4f306061
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49276958"
---
# <a name="idebugclassfieldenumconstructors"></a>IDebugClassField::EnumConstructors
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu sınıf için oluşturucuları için bir numaralandırıcı oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT EnumConstructors(   
   CONSTRUCTOR_ENUM   cMatch,  
   IEnumDebugFields** ppEnum  
);  
```  
  
```csharp  
int EnumConstructors(  
   CONSTRUCTOR_ENUM     cMatch,   
   out IEnumDebugFields ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cMatch`  
 [in] Bir değer [CONSTRUCTOR_ENUM](../../../extensibility/debugger/reference/constructor-enum.md) oluşturucular için sabit listesi türünü belirten sabit listesi.  
  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) oluşturucular listesini temsil eden nesne. Hiç Oluşturucusu yoksa null değeri döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür veya hiç Oluşturucusu varsa S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Her öğenin sabit bir [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md) Oluşturucu yöntemi tanımlayan nesne.  
  
 Oluşturucular listesi, genellikle derleyici tarafından sağlanan varsayılan oluşturucular içermez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)   
 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)   
 [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)   
 [CONSTRUCTOR_ENUM](../../../extensibility/debugger/reference/constructor-enum.md)

