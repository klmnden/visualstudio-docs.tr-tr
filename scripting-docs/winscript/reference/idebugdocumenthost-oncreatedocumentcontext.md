---
title: IDebugDocumentHost::OnCreateDocumentContext | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHost.OnCreateDocumentContext
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugDocumentHost::OnCreateDocumentContext
ms.assetid: 080c8604-cfd7-484e-a337-15040870e683
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c0f8ce73e05fa8dd163564184361254fd58163ee
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54096348"
---
# <a name="idebugdocumenthostoncreatedocumentcontext"></a>IDebugDocumentHost::OnCreateDocumentContext
Konağın, yeni bir belge bağlamına oluşturulmakta olduğundan ve isteğe bağlı olarak yeni bağlam için bilinmeyen denetleme döndürmek konak sağlar bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnCreateDocumentContext(  
   IUnknown**  ppunkOuter  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppunkOuter`  
 [out] Yeni bağlam denetleyen bir nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_NOTIMPL`|Konak, bir denetim nesnesi sağlamaz.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem Yardımcısı tarafından sağlanan belge bağlamı için yeni işlevler eklenecek konak sağlar. Bu yöntem döndürebilir **E_NOTIMPL** veya çalışması çağıran olduğu bağlamı oluşturmaktan sorumlu bir null bir dış nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentHost Arabirimi](../../winscript/reference/idebugdocumenthost-interface.md)