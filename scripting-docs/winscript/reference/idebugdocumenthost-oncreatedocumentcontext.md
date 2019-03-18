---
title: IDebugDocumentHost::OnCreateDocumentContext | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: a3b614cdc6aad17ab3a4f6e83927b59390005ac2
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58152207"
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