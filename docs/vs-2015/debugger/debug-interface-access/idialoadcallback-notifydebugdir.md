---
title: Idialoadcallback::notifydebugdir | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::NotifyDebugDir method
ms.assetid: bd04e2f6-0dbf-4742-a556-96f2cd99aa19
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2e8fe8ffe9d7d495e40c8c84b08aeaefb03e8d17
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752283"
---
# <a name="idialoadcallbacknotifydebugdir"></a>IDiaLoadCallback::NotifyDebugDir
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklama dizini .exe dosyasında bulundu çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT NotifyDebugDir (   
   BOOL  fExecutable,  
   DWORD cbData,  
   BYTE  data[]  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `fExecutable`  
 [in] `TRUE` hata ayıklama dizini, yürütülebilir bir dosya (.dbg Dosya yerine) salt okunur ise.  
  
 `cbData`  
 [in] Hata ayıklama dizininde bulunan verileri baytlık sayısı.  
  
 `data[]`  
 [in] Oturum hata ayıklama dizini doldurulmuş bir dizi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Dönüş kodu genellikle göz ardı edilir.  
  
## <a name="remarks"></a>Açıklamalar  
 [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yürütülebilir dosya işlenirken bir hata ayıklama dizini bulduğunda, bu geri çağırma yöntemini çağırır.  
  
 Bu yöntem, hata ayıklama bilgisi .pdb dosyasında bulunan dışındaki desteklemek için istemcinin ters mühendislik hata ayıklama ve/veya yürütülebilir dosya ihtiyacını ortadan kaldırır. Bu verilerle istemcide kullanılabilir hata ayıklama bilgilerinin türünü ve bu yürütülebilir dosya veya .dbg dosyasında bulunan tanıyabilirsiniz.  
  
 Çoğu istemci çünkü bu geri çağırma gerekmeyeceğinden `IDiaDataSource::loadDataForExe` yöntemi .pdb hem .dbg dosyaları sembolleri sunmak için gerekli olduğunda şeffaf bir şekilde açılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idialoadcallback2](../../debugger/debug-interface-access/idialoadcallback2.md)   
 [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)
