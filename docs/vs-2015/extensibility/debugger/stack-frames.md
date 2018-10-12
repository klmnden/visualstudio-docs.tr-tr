---
title: Yığın çerçevesi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- stack frames, debugging
- debugging [Debugging SDK], stack frames
- stack frames
ms.assetid: b5e439d4-1e9d-4e13-9cad-bb8b136d4ca8
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 301a782ebf0eda9b1e97c9f0f09c10a0985de4c2
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49271602"
---
# <a name="stack-frames"></a>Yığın Çerçeveleri
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı mimarisi bakımından bir **yığın çerçevesi**:  
  
-   Bir iş parçacığı yürütme bağlamı sağlayan bir yığının bir soyutlamadır. Bir iş parçacığı her zaman içinde bir işlevi yürütür. Bir yığın çerçevesi için işlevi ve bağımsız değişkenler, yerel değişkenleri tutar. Visual Studio ile hata ayıklamak için dil veya ortam ayıklanan yığın çerçeveleri desteklemesi gerekir.  
  
-   İçin her ikisi de tanımlamak ve kendisini açıklar ve ilişkili iş parçacığı döndürebilir. Bir yığın çerçevesi, dosyadaki geçerli yönerge işaretçisini yanı sıra ilgili belgeleri gösteren kod bağlamı ve ifade değerlendirme bağlamı da döndürebilir.  
  
-   Adı, türü ve değeri yerel değişkenleri ve bağımsız değişkenleri açıklar ve çeşitli IDE hata ayıklama pencerelerinde göründüğü özellikleri vardır.  
  
-   Tarafından temsil edilen bir [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md) arabirimi, genellikle bir hata ayıklama altyapısı (DE) veya bir iş parçacığının söz konusu kümelerdeki sanal makine tarafından oluşturuldu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)   
 [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md)

