---
title: Idiareadexeatoffsetcallback::readexecutableat | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaReadExeAtOffsetCallback::ReadExecutableAt method
ms.assetid: 30b1cef0-b366-4712-8e89-d21f640964f8
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1ac5452437ab6fdec3eb68baf46aeeab8434df4e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54757425"
---
# <a name="idiareadexeatoffsetcallbackreadexecutableat"></a>IDiaReadExeAtOffsetCallback::ReadExecutableAt
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirtilen sayıda baytı bir yürütülebilir dosya öğesinden belirtilen bir uzaklık başlayarak okur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT ReadExecutableAt (   
   DWORDLONG fileOffset,  
   DWORD     cbData,  
   DWORD*    pcbData,  
   BYTE      data[]  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 fileOffset  
 [in] Okumanın başlatılacağı çalıştırılabilir dosyadaki uzaklık.  
  
 cbData  
 [in] Okunacak bayt sayısı.  
  
 pcbData  
 [out] Okunan bayt sayısını döndürür.  
  
 veri]  
 [out içinde] Dosyadan okunan bayt ile doldurulmuş bir dizi.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bir mutlak dosya uzaklık kullanılarak çalıştırılabilir veri baytı yüklenecek DIA destek kod tarafından çağrılır. Support, bu yöntem çağrılır [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiareadexeatoffsetcallback](../../debugger/debug-interface-access/idiareadexeatoffsetcallback.md)   
 [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)
