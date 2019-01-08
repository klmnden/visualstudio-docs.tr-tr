---
title: IDispatchEx::GetDispID | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispatchEx.GetDispID
apilocation:
- scrobj.dll
helpviewer_keywords:
- GetDispID method
ms.assetid: a288d63d-b08a-4540-9d9d-0bcd182eff9a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c466ec767be53d100b970314bf0d81d5dd9dfb20
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097545"
---
# <a name="idispatchexgetdispid"></a>IDispatchEx::GetDispID
Arka arkaya çağrı kullanılabilir, karşılık gelen DISPID tek üye adı eşlendiği `IDispatchEx::InvokeEx`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetDispID(  
   BSTR bstrName,  
   DWORD grfdex,  
   DISPID *pid  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `bstrName`  
 Eşleştirilecek adı geçirildi.  
  
 `grfdex`  
 Üye tanımlayıcısını almak için seçenekleri belirler. Bu, aşağıdaki değerleri birleşimi olabilir:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|fdexNameCaseSensitive|Ad arama, büyük küçük harfe duyarlı bir şekilde yapılması istekler. Büyük küçük harfe duyarlı arama desteklemeyen nesnesiyle yoksayılabilir.|  
|fdexNameEnsure|Üye zaten yoksa, oluşturulmuş olmasını ister. Yeni üye değeri ile oluşturulması gereken `VT_EMPTY`.|  
|fdexNameImplicit|Çağıranın temel nesne açıkça belirtilmediğinde belirli bir adı bir üyesi için nesneleri arıyor gösterir.|  
|fdexNameCaseInsensitive|Ad arama, büyük küçük harf duyarsız bir şekilde yapılması istekler. Büyük küçük harf duyarsız arama desteklemeyen nesnesiyle yoksayılabilir.|  
  
 `pid`  
 DISPID sonucu almak için çağırıcı tarafından ayrılan konuma işaretçisi. Bir hata oluşursa `pid` DISPID_UNKNOWN içerir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|||  
|-|-|  
|`S_OK`|Başarılı.|  
|`E_OUTOFMEMORY`|Bellek yetersiz.|  
|`DISP_E_UNKNOWNNAME`|Adı bilinmiyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 `GetDispID` yerine kullanılan `GetIDsOfNames` DISPID için belirtilen bir üyenin elde edilir.  
  
 Çünkü `IDispatchEx` eklenmesini ve üyelerinin DISPID değeri kümesini silme değil kalan sabit bir nesne ömrü boyunca sağlar.  
  
 Kullanılmayan `riid` parametresinde `IDispatch::GetIDsOfNames` kaldırıldı.  
  
## <a name="example"></a>Örnek  
  
```cpp
BSTR bstrName;  
   DISPID dispid;  
   IDispatchEx *pdex;   
  
   // Assign to pdex and bstrName  
   pdex->GetDispID(bstrName, fdexNameCaseSensitive, &dispid);  
   // Use dispid  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDispatchEx Arabirimi](../../winscript/reference/idispatchex-interface.md)