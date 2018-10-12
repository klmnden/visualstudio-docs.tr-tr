---
title: IDiaPropertyStorage::ReadMultiple | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadMultiple
ms.assetid: 6ccc9397-ce41-4f72-b261-72ac252cd4a5
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c9ebfe7825dbf4690246d6a7fc2e67a84c850a96
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49230821"
---
# <a name="idiapropertystoragereadmultiple"></a>IDiaPropertyStorage::ReadMultiple
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Okuma özellikleri geçerli özellik kümesinden belirtildi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT ReadMultiple(   
   ULONG          cpspec,  
   PROPSPEC const rgpspec,  
   PROPVARIANT    rgvar  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cpspec`  
 [in] Belirtilen özellikleri sayısı `rgpspec` dizisi. Sıfır ise, yöntem hiçbir özellik döndürür ancak iade `S_OK` bir başarı kodu olarak.  
  
 `rgpspec`  
 [in] Okunacak özellikleri dizisi. Özellikler, bir özellik kimliği veya isteğe bağlı dize adı belirtilebilir. Dizideki herhangi belirli bir sırada özelliklerini belirtmek gerekli değildir. Dizi basit özellikleri için döndürülecek yinelenen özellik değerlerini bunun sonucunda yinelenen özellikler içerebilir. Basit olmayan özellikler, bunları ikinci kez açmak için bir denemede erişim reddedildi döndürmelidir. Dizi özelliği kimlikleri ve dize bir karışımını içerebilir. Bu dizi en az olmalıdır `cpspec` özellik değerlerini sayısı.  
  
 `rgvar`  
 [out içinde] Bir dizi `PROPVARIANT` yapıları (Microsoft.VisualStudio.OLE.Interop ad alanında) her bir özellik için değerlerle doldurulacak. Dizi en az olmalıdır `cpspec` öğeleri boyutu. Çağıranın dizideki değerleri başlatma gerekmez.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` , bir veya daha fazla özellik bulunamadı. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir özellik bulunamadı varsa, karşılık gelen bir giriş `rgvar` dizi içeren bir `VARIANT` türüyle `VT_EMPTY`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)



