---
title: IDebugDocumentHelper::DefineScriptBlock | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHelper.DefineScriptBlock
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentHelper::DefineScriptBlock
ms.assetid: e4120377-f04f-44b1-950b-2beba06c9c12
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2a320e4e43a983ace4decbaa68de0b1a7df7d457
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144569"
---
# <a name="idebugdocumenthelperdefinescriptblock"></a>IDebugDocumentHelper::DefineScriptBlock
Yardımcıya belirli bir karakter aralığı belirtilen betik altyapısı tarafından işlenen bir betik bloğu olduğunu gösterir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT DefineScriptBlock(  
   ULONG           ulCharOffset,  
   ULONG           cChars,  
   IActiveScript*  pas,  
   BOOL            fScriptlet,  
   DWORD_PTR*      pdwSourceContext  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ulCharOffset`  
 [in] Betik bloğundaki başlangıç konumu.  
  
 `cChars`  
 [in] Betik bloğundaki karakter sayısı.  
  
 `pas`  
 [in] Bu betik bloğu için komut dosyası motoru.  
  
 `fScriptlet`  
 [in] Betik bloğundaki bir kod oluşturma yöntemi olup olmadığını gösteren bayrak.  
  
 `pdwSourceContext`  
 [out] Betik bloğundaki kaynak bağlamı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Ekli komut dosyası blokları belgelerini içeren bir akıllı ana bilgisayar bu yöntemi kullanabilirsiniz. Diğer diller için katıştırılmış betik kodunu içerdiğinde, bir dil altyapısı bu yöntemi kullanabilirsiniz.  
  
 Komut dosyası altyapısı, tüm söz dizimi renklendirme ve kod bağlamı aramaları betik bloğundaki sorumludur.  
  
 `DefineScriptBlock` Metin eklendikten sonra yöntemi'nin çağrılabilir (örnek olarak, `IDebugDocumentHelper::AddDBCSText` yöntemi), ancak önce betik bloğu ayrıştırıldıktan (örnek olarak, `IActiveScriptParse ::ParseScriptText` yöntemi).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugdocumenthelper arabirimi](../../winscript/reference/idebugdocumenthelper-interface.md)   
 [IDebugDocumentHelper::AddDBCSText](../../winscript/reference/idebugdocumenthelper-adddbcstext.md)   
 [IDebugDocumentHelper::AddUnicodeText](../../winscript/reference/idebugdocumenthelper-addunicodetext.md)