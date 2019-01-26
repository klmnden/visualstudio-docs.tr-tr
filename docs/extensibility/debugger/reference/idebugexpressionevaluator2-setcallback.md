---
title: IDebugExpressionEvaluator2::SetCallback | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugExpressionEvaluator2::SetCallback
- SetCallback
ms.assetid: 31e3a99e-e784-44a3-8b19-cc5ef31ed546
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 571fe8085dc07ff32fa8a253c99cb9a0790120bb
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54974246"
---
# <a name="idebugexpressionevaluator2setcallback"></a>IDebugExpressionEvaluator2::SetCallback
Hata ayıklayıcısı altyapısı (DE), ölçüm ayarları okumak için kullanacağı bir geri arama arabirimini belirtmek ifade değerlendirici (EE) sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT SetCallback (  
   IDebugSettingsCallback2* pCallback  
);  
```  
  
```csharp  
int SetCallback (  
   IDebugSettingsCallback2 pCallback  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pCallback`  
 [in] İçin ayarları geri çağırma kullanmak için arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bir ifade değerlendiricisi ölçüm ayarları okumak için kullanabileceğiniz oturum hata ayıklama Yöneticisi için bir arabirim sağlar. Ölçümler üzerinde okumak için uzaktan hata ayıklama içinde yararlıdır [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] bilgisayar.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekler için bu yöntemi uygulamak nasıl gösterir bir **CEE** gösteren nesne [IDebugSettingsCallback2](../../../extensibility/debugger/reference/idebugsettingscallback2.md) arabirimi.  
  
```cpp  
HRESULT CEE::SetCallback(IDebugSettingsCallback2* in_pCallback)  
{  
    // precondition  
    INVARIANT( this );  
  
    // function body  
    if (NULL != this->m_LanguageSpecificUseCases.pfSetCallback)  
    {  
        EEDomain::fSetCallback DomainVal =  
        {  
            in_pCallback  
        };  
  
        BOOL bSuccess = (*this->m_LanguageSpecificUseCases.pfSetCallback)(DomainVal);  
        ENSURE( bSuccess );  
    }  
  
    // postcondition  
    INVARIANT( this );  
  
    return S_OK;  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugExpressionEvaluator2](../../../extensibility/debugger/reference/idebugexpressionevaluator2.md)