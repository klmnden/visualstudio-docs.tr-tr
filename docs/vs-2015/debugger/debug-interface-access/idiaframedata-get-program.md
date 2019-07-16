---
title: Idiaframedata::get_program | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::get_program method
ms.assetid: 9201409e-b4b1-4e2e-a9f8-d17678ac538b
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d87f5c7fda25a901d44b9f511b9a92eb4471f845
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68180008"
---
# <a name="idiaframedatagetprogram"></a>IDiaFrameData::get_program
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Geçerli işlevi çağırmadan önce ayarlanmış kayıt hesaplamak için kullanılan program dizesini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT get_program (   
   BSTR* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Program dizeyi döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Program dize prolog kurulabilmesi yorumlanır makroları dizisidir. Örneğin, tipik bir yığın çerçevesi program dize kullanabilirsiniz `"$T0 $ebp = $eip $T0 4 + ^ = $ebp $T0 ^ = $esp $T0 8 + ="`. Burada işleçler işlenenlerin izleyin, ters Lehçe gösterimi biçimidir. `T0` geçici bir değişkende temsil eder. Bu örnek, aşağıdaki adımları gerçekleştirir:  
  
1. Kaydının içeriğini taşımak `ebp` için `T0`.  
  
2. Ekleme `4` değerine `T0` bir adresi üretmek, adresten değeri Al ve kayıttaki değeri depolamak için `eip`.  
  
3. Depolanan adresinden değer elde `T0` ve kayıttaki değeri depola `ebp`.  
  
4. Ekleme `8` değerine `T0` ve kayıttaki değeri depola `esp`.  
  
   Program dize CPU ve geçerli yığın çerçevesi tarafından temsil edilen işlev için ayarlanan çağırma kuralı için özel olduğunu unutmayın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)
