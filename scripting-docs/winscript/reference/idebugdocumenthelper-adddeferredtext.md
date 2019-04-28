---
title: IDebugDocumentHelper::AddDeferredText | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHelper.AddDeferredText
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentHelper::AddDeferredText
ms.assetid: 9463cfb0-76cc-45ee-b32c-f37dce2b2e0e
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b2f2a7c134142668613cc38cee9357e42cb95096
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63433937"
---
# <a name="idebugdocumenthelperadddeferredtext"></a>IDebugDocumentHelper::AddDeferredText
Verilen metni kullanılabilir, ancak karakterleri sağlamaz yardımcı bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AddDeferredText(  
   ULONG  cChars,  
   DWORD  dwTextStartCookie  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cChars`  
 [in] Eklenecek karakter (Unicode) sayısı.  
  
 `dwTextStartCookie`  
 [in] Metnin başlangıç konumunu temsil eden ana bilgisayar tanımlı tanımlama bilgisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_FAIL`|Yöntem başarısız oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, doğru bildirimleri ve boyut bilgileri oluşturmak yardımcıyı verirken gerekene kadar eklemek için karakter sağlama erteleneceği konak sağlar. `dwTextStartCookie` Metnin başlangıç konumunu temsil eden konak tarafından tanımlanan bir tanımlama bilgisi parametredir. Yapılan sonraki çağrılar `IDebugDocumentText::GetText` bu tanımlama bilgisini belirtmeniz gerekir. Örneğin, DBCS içinde metin temsil eden bir ana bilgisayar, bir bayt uzaklığı tanımlama bilgisi olabilir.  
  
 Varsayılır tek bir çağrı `IDebugDocumentText::GetText` karakter birden çok çağrı alabilirsiniz `AddDeferredText`. Yardımcı sınıfları da birden çok kez aynı ertelenmiş karakter aralığının isteyebilir.  
  
> [!NOTE]
> Çağrılar `AddDeferredText` çağrılarıyla karma olmayan `AddUnicodeText` veya `AddDBCSText`. Bu meydana gelirse, `E_FAIL` döndürülür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugdocumenthelper arabirimi](../../winscript/reference/idebugdocumenthelper-interface.md)   
 [IDebugDocumentHelper::AddUnicodeText](../../winscript/reference/idebugdocumenthelper-addunicodetext.md)   
 [IDebugDocumentHelper::AddDBCSText](../../winscript/reference/idebugdocumenthelper-adddbcstext.md)   
 [IDebugDocumentText::GetText](../../winscript/reference/idebugdocumenttext-gettext.md)