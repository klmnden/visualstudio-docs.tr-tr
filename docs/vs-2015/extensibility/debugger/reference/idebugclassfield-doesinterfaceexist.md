---
title: IDebugClassField::DoesInterfaceExist | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugClassField::DoesInterfaceExist
helpviewer_keywords:
- IDebugClassField::DoesInterfaceExist method
ms.assetid: cc0c8642-1a76-4fda-a309-7018a34883c9
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 9f71346c1b69729ae54ef0d33be4149e7000316c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54779897"
---
# <a name="idebugclassfielddoesinterfaceexist"></a>IDebugClassField::DoesInterfaceExist
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Belirli bir arabirim sınıfta tanımlı olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT DoesInterfaceExist(   
   LPCOLESTR pszInterfaceName  
);  
```  
  
```csharp  
int DoesInterfaceExist(  
   [In] string pszInterfaceName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszInterfaceName`  
 [in] Arabirim adı, aranacak içeren bir dize.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür, S_FALSE döndürür arabirimi yoksa, Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, geçerli tüm arabirimleri numaralandırmasını alır ve eşleşen bir arabirim için liste arar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)
