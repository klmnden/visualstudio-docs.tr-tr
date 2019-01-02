---
title: IDebugDocumentPositionOffset2::GetRange | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugDocumentPositionOffset2::GetRange
ms.assetid: 27da7130-0932-4f97-abde-05e6fb018606
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7f780d5df2d111a371a4389cd29d4b724dfe3834
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53855263"
---
# <a name="idebugdocumentpositionoffset2getrange"></a>IDebugDocumentPositionOffset2::GetRange
Geçerli belge konumunu aralığını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetRange(  
   DWORD* pdwBegOffset,  
   DWORD* pdwEndOffset  
);  
```  
  
```csharp  
public int GetRange(  
   ref uint pdwBegOffset,  
   ref uint pdwEndOffset  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pdwBegOffset`  
 [out içinde] Aralık için başlangıç konumu uzaklığı. Bu bilgiler gerekli değildir, bu parametre null bir değere ayarlayın.  
  
 `pdwEndOffset`  
 [out içinde] Aralığın bitiş konumu için uzaklık. Bu bilgiler gerekli değildir, bu parametre null bir değere ayarlayın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir konum kesme noktası için bir belge konumda belirtilen aralık gerçekten kod katkıda bulunan bir deyim için önceden aramak için hata ayıklama altyapısı (DE) kullanılır. Örneğin, aşağıdaki kodu düşünün:  
  
```  
Line 5: // comment  
Line 6: x = 1;  
```  
  
 Satır 5 kod hata ayıklaması yapılan programa katkıda bulunur. 5. satırda bir kesme noktası ayarlar hata ayıklayıcı belirli bir miktar kod katkıda bulunan ilk satır için ileriye doğru arama için DE isterse, hata ayıklayıcı bir kesme noktası burada doğru yerleştirilebileceği ek aday satırları içeren bir aralık belirtmeniz gerekir. Bir kesme noktası kabul edebilecek bir satırı bulunan kadar DE ardından İleri bu satırlar arama.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentPositionOffset2](../../../extensibility/debugger/reference/idebugdocumentpositionoffset2.md)   
 [GetRange](../../../extensibility/debugger/reference/idebugdocumentposition2-getrange.md)