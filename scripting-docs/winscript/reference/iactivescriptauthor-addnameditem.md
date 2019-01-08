---
title: IActiveScriptAuthor::AddNamedItem | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthor.AddNamedItem
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthor::AddNamedItem
ms.assetid: 951003b6-1c4a-4086-b7ce-2f128e007280
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 85c434ea17d41fb98300289c3161349f9d9f5a2f
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54094867"
---
# <a name="iactivescriptauthoraddnameditem"></a>IActiveScriptAuthor::AddNamedItem
Komut dosyası altyapısının ad alanı yazma kök düzeyinde öğe adını ekler. A *kök düzeyinde öğe* özellikleri ve yöntemleri içerebilir ve bu de içerebilir bir olay kaynağı bir nesnedir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AddNamedItem(  
   LPCOLESTR          pszName,  
   DWORD              dwFlags,  
   IDispatch          *pdisp  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszName`  
 [in] Betikten göründüğü haliyle öğesi adı. Ad benzersiz ve kalıcı olması gerekir.  
  
 `dwFlags`  
 [in] Adlandırılmış öğeyle ilişkili bayraklar. Aşağıdaki değerlerin bir birleşimi olabilir:  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|SCRIPTITEM_ISVISIBLE|0x00000002|Öğenin adı komut dosyası ad alanında kullanılabilir olduğunu gösterir. Bu öğenin özellikleri, yöntemleri ve olaylara erişim sağlar.<br /><br /> Kural gereği, öğenin alt üyeleri öğesinin özelliklerini içerir. Bu nedenle, tüm alt nesne özellikleri ve yöntemleri (ve alt üyelerinin özyinelemeli olarak) erişilebilir.|  
|SCRIPTITEM_ISSOURCE|0x00000004|Komut betiği olay işleyicileri olabilir öğe kaynağının olayları gösterir.|  
|SCRIPTITEM_GLOBALMEMBERS|0x00000008|Öğesi genel özellikleri ve komut dosyası ile ilişkili olan yöntemleri koleksiyonu olduğunu gösterir. Üyeleri, genel değişkenler ve yöntemler denetlenir.|  
|SCRIPTITEM_ISPERSISTENT|0x00000040|Komut dosyası altyapısı yazma kaydedilirse öğesi kaydedilmesi gerektiğini gösterir.|  
|SCRIPTITEM_CODEONLY|0x00000200|Adlandırılmış öğe yalnızca kod bir nesneyi temsil eder ve yazmak için bir üye yok gösterir.|  
|SCRIPTITEM_NOCODE|0x00000400|Adlandırılmış öğe eklenen bir ad ve yazmak için hiçbir şey sahip olduğunu gösterir.|  
  
 `pdisp`  
 [in] `IDispatch` , `NamedItem` Yöntemler, özellikler veya olay kaynağı toplamak için kullanılan nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptauthor arabirimi](../../winscript/reference/iactivescriptauthor-interface.md)   
 [IActiveScriptAuthor::RemoveNamedItem](../../winscript/reference/iactivescriptauthor-removenameditem.md)