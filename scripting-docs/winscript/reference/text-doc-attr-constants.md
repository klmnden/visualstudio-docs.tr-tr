---
title: TEXT_DOC_ATTR sabitleri | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- TEXT_DOC_ATTR
apilocation:
- scrobj.dll
helpviewer_keywords:
- TEXT_DOC_ATTR constants
ms.assetid: fd9c53a4-8f73-4c6a-abe5-6b831ecd5b1e
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d22b178d85d304f19e52727ef2c67d77f16da1b3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62840089"
---
# <a name="textdocattr-constants"></a>TEXT_DOC_ATTR Sabitleri
Belgenin özniteliklerini açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef DWORD TEXT_DOC_ATTR;  
```  
  
## <a name="constants"></a>Sabitler  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|TEXT_DOC_ATTR_READONLY|0x00000001|Belge salt okunur.|  
|TEXT_DOC_ATTR_TYPE_PRIMARY|0x00000002|Belge, bu belge ağacının birincil dosyasıdır.|  
|TEXT_DOC_ATTR_TYPE_WORKER|0x00000004|Bir çalışan belgesidir.|  
|TEXT_DOC_ATTR_TYPE_SCRIPT|0x00000008|Belge, bir komut dosyasıdır.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Hata Ayıklayıcı Sabitleri, Sabit Listeleri ve Yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)