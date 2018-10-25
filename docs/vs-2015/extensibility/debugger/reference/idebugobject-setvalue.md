---
title: IDebugObject::SetValue | Microsoft Docs
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
- IDebugObject::SetValue
helpviewer_keywords:
- IDebugObject::SetValue method
ms.assetid: d652e09c-cdc1-4519-8116-d7c743f5679b
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a8811fcdc4caef62cb3973364b4b8b594d83936d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49885076"
---
# <a name="idebugobjectsetvalue"></a>IDebugObject::SetValue
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nesnenin değerini ardışık bir bayt serisinden ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT SetValue(   
   BYTE* pValue,  
   UINT  nSize  
);  
```  
  
```csharp  
int SetValue(  
   byte[] pValue,   
   uint   nSize  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pValue`  
 [in] Yeni değeri temsil eden bir bayt dizisi.  
  
 `nSize`  
 [in] Değerin bayt cinsinden boyutu.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Dizideki değerleri bu kopyalanır [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) herhangi bir mevcut değer değiştirme, nesne. Yeni değer boyutu, mevcut değerinden küçük veya çok büyük olabilir. Bu `IDebugObject` bir null başvuru olamaz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)   
 [GetValue](../../../extensibility/debugger/reference/idebugobject-getvalue.md)

