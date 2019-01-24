---
title: IDebugPortSupplier3::EnumPersistedPorts | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPortSupplier3::EnumPersistedPorts
helpviewer_keywords:
- IDebugPortSupplier3::EnumPersistedPorts
ms.assetid: 1c3dead3-5d6c-4067-8418-4015f0b0dd07
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 944159ead89166c8452775bd6522a7c441094ad0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54784969"
---
# <a name="idebugportsupplier3enumpersistedports"></a>IDebugPortSupplier3::EnumPersistedPorts
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, kalıcı bağlantı noktalarının listesi numaralandırmasına izin veren bir nesneyi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumPersistedPorts(  
   BSTR_ARRAY         PortNames,  
   IEnumDebugPorts2** ppEnum  
);  
```  
  
```csharp  
int EnumPersistedPorts(  
   BSTR_ARRAY           PortNames,  
   out IEnumDebugPorts2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `PortNames`  
 [in] A [BSTR_ARRAY](../../../extensibility/debugger/reference/bstr-array.md) bulun ve kalıcı bağlantı noktaları arasında döndürmek için bağlantı noktası adları listesini içeren yapısı. Yalnızca kalıcı bağlantı noktalarından şu adlara sahip döndürülür.  
  
 `ppEnum`  
 [out] Uygulayan bir nesne [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md) arabirimi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bağlantı noktası sağlayıcısı örneği ve bağlantı noktası sağlayıcısı kaldırıldığında kaydedilen kalıcı bağlantı noktaları yüklenir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortSupplier3](../../../extensibility/debugger/reference/idebugportsupplier3.md)   
 [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md)   
 [BSTR_ARRAY](../../../extensibility/debugger/reference/bstr-array.md)
