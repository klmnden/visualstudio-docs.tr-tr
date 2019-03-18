---
title: DebugStackFrameDescriptor yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- DebugStackFrameDescriptor
apilocation:
- scrobj.dll
helpviewer_keywords:
- DebugStackFrameDescriptor structure
ms.assetid: a86bcb99-41e4-4a26-a1dd-e1458fb73139
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fddae48178ec6c56ce647f5c4f3a1bff3d81a980
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58153324"
---
# <a name="debugstackframedescriptor-structure"></a>DebugStackFrameDescriptor Yapısı
Yığın çerçevelerini listeler ve aynı iş parçacığındaki çeşitli listeleyicilerden alınan çıktıyı birleştirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef struct tagDebugStackFrameDescriptor {  
   IDebugStackFrame *pdsf;  
   DWORD_PTR        dwMin;  
   DWORD_PTR        dwLim;  
   BOOL             fFinal;  
   IUnknown         *punkFinal;  
} DebugStackFrameDescriptor;  
```  
  
## <a name="members"></a>Üyeler  
 `pdsf`  
 Yığın çerçeve nesnesi.  
  
 `dwMin`  
 Bu yığın çerçevesiyle ilişkili fiziksel adreslerini alt aralığı makine bağımlı gösterimi.  
  
 `dwLim`  
 Bu yığın çerçevesiyle ilişkili fiziksel adreslerini üst aralığının makine bağımlı gösterimi.  
  
 `fFinal`  
 Çerçeve işlenmekte olduğunu gösteren bayrak.  
  
 `punkFinal`  
 Bu parametre değilse `NULL`, birleştirme geçerli Numaralandırıcı durdurmanız gerekir ve yeni bir tane başlatılmış olması. Nesnesine yeni bir sabit listesini Başlat nasıl gösterir.  
  
## <a name="remarks"></a>Açıklamalar  
 İşlem Hata Ayıklama Yöneticisi, birden çok komut dosyası motorları yığın çerçevelerini sıralamak için bu yapıyı kullanır. Kural gereği, aşağı yığınları büyütün. Sonuç olarak, burada yığınları büyütün mimarilerde yuvarlandığında tamamlanan adresleri olmalıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Hata Ayıklayıcı Sabitleri, Sabit Listeleri ve Yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)