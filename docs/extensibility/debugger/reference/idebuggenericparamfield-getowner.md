---
title: IDebugGenericParamField::GetOwner | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugGenericParamField::GetOwner
ms.assetid: c7f6d166-a69e-40c4-bd0b-1a1fdf9aaacf
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: a05bb61d10fe7e03e5f7a46939a2ac233fa723da
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53901509"
---
# <a name="idebuggenericparamfieldgetowner"></a>IDebugGenericParamField::GetOwner
Bu genel parametre türü veya yönteminde sahibi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetOwner(  
   IDebugField** ppOwner  
);  
```  
  
```csharp  
int GetOwner(  
   out IDebugField ppOwner  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppOwner`  
 [out] Döndürür [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) bu genel parametre sahip bir nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugGenericParamFieldType** gösteren nesne [IDebugGenericParamField](../../../extensibility/debugger/reference/idebuggenericparamfield.md) arabirimi.  
  
```cpp  
HRESULT CDebugGenericParamFieldType::GetOwner(IDebugField** ppOwner)  
{  
    HRESULT hr = S_OK;  
    CComPtr<IMetaDataImport> pMetadata;  
  
    METHOD_ENTRY( CDebugGenericParamFieldType::GetOwner );  
  
    IfFalseGo(ppOwner, E_INVALIDARG );  
    *ppOwner = NULL;  
  
    IfFailGo( this->LoadProps() );  
    IfFailGo( m_spSH->GetMetadata( m_idModule, &pMetadata ) );  
  
    switch (TypeFromToken(m_tokOwner))  
    {  
        case mdtMethodDef:  
            {  
                mdTypeDef tokClass;  
                CComPtr<IDebugField> pClass;  
                CDEBUG_ADDRESS caddr;  
                CComPtr<IDebugContainerField> pContainer;  
  
                IfFailGo( pMetadata->GetMethodProps( m_tokOwner, &tokClass, NULL, 0, NULL, NULL, NULL, NULL, NULL, NULL ) );  
                IfFailGo( m_spSH->CreateClassType(m_idModule, tokClass, &pClass) );  
                IfFailGo( pClass->QueryInterface( &pContainer ) );  
                IfFailGo( caddr.InitializeMethod( m_idModule, tokClass, m_tokOwner, 0, 0 ) );  
                IfFailGo( m_spSH->CreateMethodSymbol( pContainer, caddr, FIELD_SYM_MEMBER, ppOwner ) );  
                break;  
            }  
        case mdtTypeDef:  
            {  
                IfFailGo( m_spSH->CreateClassType(m_idModule, m_tokOwner, ppOwner) );  
                break;  
            }  
        default:  
            {  
                ASSERT(!"Unexpected Owner type for Generic Param Field");  
                hr = E_FAIL;  
            }  
    }  
Error:  
  
    METHOD_EXIT( CDebugGenericParamFieldType::GetOwner, hr );  
    return hr;  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugGenericParamField](../../../extensibility/debugger/reference/idebuggenericparamfield.md)