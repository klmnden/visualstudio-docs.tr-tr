---
title: Idebugexpressioncontext::parselanguagetext | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugExpressionContext.ParseLanguageText
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugExpressionContext::ParseLanguageText
ms.assetid: 650cb016-7d80-4011-b264-780f871a3466
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 50f9f398b9193c776f8e2a823b78ce7b8da438b1
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58153480"
---
# <a name="idebugexpressioncontextparselanguagetext"></a>IDebugExpressionContext::ParseLanguageText
Belirtilen metni için bir hata ayıklama ifadesi oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ParseLanguageText(  
   LPCOLESTR           pstrCode,  
   UINT                nRadix,  
   LPCOLESTR           pstrDelimiter,  
   DWORD               dwFlags,  
   IDebugExpression**  ppe  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrCode`  
 [in] İfadeyi veya deyim metni sağlar.  
  
 `nRadix`  
 [in] Kullanılacak sayı tabanı.  
  
 `pstrDelimiter`  
 [in] Sonlandırma, betik bloğu sınırlayıcı. Zaman `pstrCode` ayrıştırılır metin akışından gibi iki betik bloğunun sonu algılamak için tırnak işaretleri ("), tek bir ana bilgisayar genellikle bir ayırıcı kullanır. Bu parametre, bazı koşullu ilkel bir ön işleme sağlamak komut dosyası altyapısı verme konak kullanılan sınırlayıcıyı belirtir (örneğin, tek tırnak işaretini ['] ayırıcı olarak kullanılacak iki tek tırnak işaretleri yerine). Tam olarak nasıl (ve ise) bu bilgileri komut dosyası altyapısına bağlıdır komut dosyası altyapısı kullanır. Bu parametre kümesine `NULL` konak betik bloğunun sonu işaretlemek için sınırlayıcı kullanmadıysanız.  
  
 `dwFlags`  
 [in] Aşağıdaki hata ayıklama metin bayrakların birleşimi:  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|DEBUG_TEXT_ISEXPRESSION|0x00000001|Metin bir ifadenin bir deyim aksine olduğunu gösterir. Bu bayrak, metin bazı diller tarafından ayrıştırılır şekilde etkileyebilir.|  
|DEBUG_TEXT_RETURNVALUE|0x00000002|Dönüş değeri varsa, çağıran tarafından kullanılır.|  
|DEBUG_TEXT_NOSIDEEFFECTS|0x00000004|Yan etkileri izin vermez. İfadenin değerlendirilmesi, bu bayrağı ayarlarsanız, hiçbir çalışma zamanı durumu değiştirmeniz gerekir.|  
|DEBUG_TEXT_ALLOWBREAKPOINTS|0x00000008|Metin değerlendirmesi sırasında kesme noktaları sağlar. Bu bayrak ayarlanmazsa kesme noktaları metin değerlendirmesi sırasında dikkate alınmaz.|  
|DEBUG_TEXT_ALLOWERRORREPORT|0x00000010|Hata raporlarını metin değerlendirmesi sırasında sağlar. Ardından bu bayrağı ayarlanmamışsa hata konağa değerlendirmesi sırasında raporlanmaz.|  
|DEBUG_TEXT_EVALUATETOCODECONTEXT|0x00000020|Deyimi çalıştırmak yerine bir kod içeriği için değerlendirilecek ifade olduğunu gösterir|  
  
 `ppe`  
 [out] Belirtilen metin için hata ayıklama ifade döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, belirtilen metnin bir hata ayıklama ifadesi oluşturur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugExpressionContext Arabirimi](../../winscript/reference/idebugexpressioncontext-interface.md)