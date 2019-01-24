---
title: IDebugProcessSecurity::QueryCanSafelyAttach | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugProcessSecurity::QueryCanSafelyAttach
ms.assetid: 63ec1ae8-27da-4574-aa15-1c986fe9fe58
caps.latest.revision: 5
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d32cd1222d9c6580efab97f38ff924e320c42b42
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754364"
---
# <a name="idebugprocesssecurityquerycansafelyattach"></a>IDebugProcessSecurity::QueryCanSafelyAttach
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, kullanıcının güvenli olmayan bir işleme iliştirir önce bir uyarı görüntülenecek bağlantı noktası sağlayıcısı sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT QueryCanSafelyAttach();  
```  
  
```csharp  
int QueryCanSafelyAttach();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Dönüş değerleri aşağıdaki gibidir:  
  
-   `S_OK`: İşlemine iliştirme güvenlidir ve uyarı iletişim kutusu gösterilir.  
  
-   `S_FALSE`: İliştirme bir güvenlik sorunu olabilir ve bir uyarı ile bir iletişim kutusu gösterilir.  
  
-   `FAILURE`: İşlemine iliştirme başarısız.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcessSecurity](../../../extensibility/debugger/reference/idebugprocesssecurity.md)
