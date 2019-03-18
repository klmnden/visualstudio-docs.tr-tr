---
title: IDebugDocumentHost::GetDeferredText | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHost.GetDeferredText
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugDocumentHost::GetDeferredText
ms.assetid: 527da666-fef5-4db3-a319-e68d466a7721
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f20b090f880168b3561cba547db319813ba3fe02
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58148079"
---
# <a name="idebugdocumenthostgetdeferredtext"></a>IDebugDocumentHost::GetDeferredText
Kullanılarak eklenmiş olan karakter aralığı döndürür `IDebugDocumentHelper::AddDeferredText` özgün ana bilgisayar belgedeki yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetDeferredText(  
   DWORD              dwTextStartCookie,  
   WCHAR*             pcharText,  
   SOURCE_TEXT_ATTR*  pstaTextAttr,  
   ULONG*             pcNumChars,  
   ULONG              cMaxChars  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwTextStartCookie`  
 [in] Metnin başlangıç konumunu temsil eden ana bilgisayar tanımlı tanımlama bilgisi.  
  
 `pcharText`  
 [out içinde] Bir karakterin metin arabelleği. Bu parametre ise bu yöntem karakterleri döndürmedi `NULL`.  
  
 `pstaTextAttr`  
 [out içinde] Bir karakter özniteliğini arabelleği. Bu parametre ise bu yöntem öznitelikleri döndürmeyen `NULL`.  
  
 `pcNumChars`  
 [out içinde] Döndürülen karakter/özniteliklerinin gerçek sayısını gösterir. Bu parametre, bu yöntemi çağırmadan önce sıfır olarak ayarlanmalıdır.  
  
 `cMaxChars`  
 [in] Döndürülecek karakterlerin sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_NOTIMPL`|Yöntem uygulanmadı.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem döndürebilir `E_NOTIMPL`, ana bilgisayar arama `IDebugDocumentHelper::AddDeferredText`.  
  
> [!NOTE]
>  Bu yöntem, özgün belgesinden metin döndürür. Konak düzenlemeler veya belge başka değişiklikler izlemek değildir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugdocumenthost arabirimi](../../winscript/reference/idebugdocumenthost-interface.md)   
 [IDebugDocumentHelper::AddDeferredText](../../winscript/reference/idebugdocumenthelper-adddeferredtext.md)   
 [SOURCE_TEXT_ATTR Sabit Listesi](../../winscript/reference/source-text-attr-enumeration.md)