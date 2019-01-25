---
title: Idiatable::Item | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaTable::Item method
ms.assetid: eae11b26-4807-400c-be25-e85bbc0c6b20
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 6112a4580a68a98407723afab1ec3310d0f1cca9
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799385"
---
# <a name="idiatableitem"></a>IDiaTable::Item
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirtilen giriş tablosundaki bir başvuru alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Item (   
   DWORD      index,  
   IUnknown** element  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `index`  
 [in] Tablo girişi için 0 aralığındaki dizinini `count`-1, burada `count` tarafından döndürülen [Idiatable::get_Count](../../debugger/debug-interface-access/idiatable-get-count.md)yöntemi.  
  
 `element`  
 [out] Döndürür bir `IUnknown` belirtilen tablo girişi temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir tablo nesnelerinin bir koleksiyonunu temsil eder. Nesnelere bağlı olarak, öğenin parametresi uygun arabirimine çevirebilirsiniz. Örneğin, bir tablo içeriyorsa [Idiasegment](../../debugger/debug-interface-access/idiasegment.md) öğesi parametresi atanabilecek sonra nesneleri `IDiaSegment` arabirimi.  
  
 Çağırmak için daha yaygın bir yaklaşımdır `QueryInterface` yönteminde [Idiatable](../../debugger/debug-interface-access/idiatable.md) uygun Numaralandırıcı arabirimi arabirim ve içindekiler erişmek için Numaralandırıcı belirli yöntemlerini kullanın. Bkz: [Idiaenumınjectedsources](../../debugger/debug-interface-access/idiaenuminjectedsources.md) örneği için arabirim.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiatable](../../debugger/debug-interface-access/idiatable.md)   
 [Idiatable::get_Count](../../debugger/debug-interface-access/idiatable-get-count.md)   
 [Idiasegment](../../debugger/debug-interface-access/idiasegment.md)   
 [IDiaEnumInjectedSources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)
