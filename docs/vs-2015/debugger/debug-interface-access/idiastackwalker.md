---
title: Idiastackwalker | Microsoft Docs
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
- IDiaStackWalker interface
ms.assetid: 4a61a22a-9cf8-4ea1-9e6e-b42f96872d40
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d888418906922e58b6d92fc3b13b8214b3d3d7c1
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49291375"
---
# <a name="idiastackwalker"></a>IDiaStackWalker
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

.pdb dosyasını bilgileri kullanarak bir yığın yapmak için yöntemleri yol sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDiaStackWalker: IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaStackWalker`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDiaStackWalker::getEnumFrames](../../debugger/debug-interface-access/idiastackwalker-getenumframes.md)|Bir yığın çerçevesi Numaralandırıcı x86 için alır platformlar.|  
|[IDiaStackWalker::getEnumFrames2](../../debugger/debug-interface-access/idiastackwalker-getenumframes2.md)|Belirli bir platform türü için bir yığın çerçevesi Numaralandırıcı alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim, yığın çerçevesi için yüklenen bir modülün listesini almak için kullanılır. Bu yöntemlerin her biri geçirilen bir [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md) (istemci uygulaması tarafından uygulanan) yığın çerçevelerini listesini oluşturmak için gereken bilgileri sağlayan nesne.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim çağırılarak alınır `CoCreateInstance` sınıf tanımlayıcısı yöntemiyle `CLSID_DiaStackWalker` ve arabirim kimliği `IID_IDiaStackWalker`. Bu örnek, bu arabirimi nasıl aldıklarına gösterir.  
  
## <a name="example"></a>Örnek  
 Bu örnek nasıl alınacağını gösterir `IDiaStackWalker` arabirimi.  
  
```cpp#  
  
      IDiaStackWalker* pStackWalker;  
HRESULT hr = CoCreateInstance(CLSID_DiaStackWalker,  
                              NULL,  
                              CLSCTX_INPROC_SERVER,  
                              IID_IDiaStackWalker,  
                              (void**) &pStackWalker);  
if (FAILED(hr))  
{  
    // Report error and exit  
}  
```  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: Dia2.h  
  
 Kitaplık: diaguids.lib  
  
 DLL: msdia80.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arabirimler (arabirim erişimi SDK'SINDA hata ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)



