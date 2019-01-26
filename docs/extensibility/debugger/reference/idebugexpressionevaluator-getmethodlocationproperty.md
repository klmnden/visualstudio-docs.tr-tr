---
title: IDebugExpressionEvaluator::GetMethodLocationProperty | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugExpressionEvaluator::GetMethodLocationProperty
helpviewer_keywords:
- IDebugExpressionEvaluator::GetMethodLocationProperty method
ms.assetid: 52c42a2e-f144-476b-8bef-442464c8fe8e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f0c8778c512719302c90e1513575714d15105ccf
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55013814"
---
# <a name="idebugexpressionevaluatorgetmethodlocationproperty"></a>IDebugExpressionEvaluator::GetMethodLocationProperty
Bu yöntem, bir bellek adresi bir yöntem konum ve uzaklık dönüştürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetMethodLocationProperty(   
   LPCOLESTR             upstrFullyQualifiedMethodPlusOffset,  
   IDebugSymbolProvider* pSymbolProvider,  
   IDebugAddress*        pAddress,  
   IDebugBinder*         pBinder,  
   IDebugProperty2**     ppProperty  
);  
```  
  
```csharp  
int GetMethodLocationProperty(  
   string               upstrFullyQualifiedMethodPlusOffset,   
   IDebugSymbolProvider pSymbolProvider,   
   IDebugAddress        pAddress,   
   IDebugBinder         pBinder,   
   out IDebugProperty2  ppProperty  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `upstrFullyQualifiedMethodPlusOffset`  
 [in] Uzaklık ve yöntemi konumunu bir dize olarak ifade.  
  
 `pSymbolProvider`  
 [in] Sembol sağlayıcısı olarak ifade edilen bir [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md) nesne.  
  
 `pAddress`  
 [in] Bir adresi olarak ifade edilen metodundaki bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) nesne.  
  
 `pBinder`  
 [in] Bağlayıcı olarak ifade edilen bir [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) nesne.  
  
 `ppProperty`  
 [out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) bellek adresini temsil eden arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Döndürülen adresi, örneğin bir kesme noktası ayarlamak için kullanılabilir.  
  
 Adına rağmen `upstrFullyQualifiedMethodPlusOffset`, bu parametre, kısmen nitelenmiş yöntem adı geçirilebilir. Bu durumda, seçilen yöntemi kapsayan sertifikadır `pAddress`. Bu parametre nasıl yorumlanacağını ifade değerlendiricisi ve desteklediği dil kadar uygulamasıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)   
 [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md)