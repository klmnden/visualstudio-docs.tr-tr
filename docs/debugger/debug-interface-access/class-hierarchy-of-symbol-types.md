---
title: Hiyerarşi Simge türlerinin sınıf | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- symbols [DIA SDK], class hierarchies
ms.assetid: 0ccd6990-4654-44cd-a6f3-bdd82fe90f6c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: fa257de86367f2531cce5c57080cd059856fa82a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53902860"
---
# <a name="class-hierarchy-of-symbol-types"></a>Simge Türlerinin Sınıf Hiyerarşisi
Aşağıdaki tabloda, sınıf hiyerarşisindeki sembol türleri açıklanmaktadır.  
  
## <a name="symbol-types"></a>Sembol türleri  
  
|Simge türü|Açıklama|  
|-----------------|-----------------|  
|[UDT](../../debugger/debug-interface-access/udt.md)|Her sınıf, yapı ve birleşim temsil etmek için kullanılan simge.|  
|[Enum (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/enum-debug-interface-access-sdk.md)|Numaralandırılmış türler simgesi.|  
|[PointerType](../../debugger/debug-interface-access/pointertype.md)|İşaretçi türleri simgesi.|  
|[ArrayType](../../debugger/debug-interface-access/arraytype.md)|Dizi türleri simgesi.|  
|[BaseType](../../debugger/debug-interface-access/basetype.md)|Temel türleri simgesi|  
|[Tür Tanımı (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/typedef-debug-interface-access-sdk.md)|Tanıtan diğer türleri için adlar simge.|  
|[BaseClass](../../debugger/debug-interface-access/baseclass.md)|Her bir kullanıcı tanımlı tür (UDT) taban sınıfı için kullanılan simge.|  
|[Arkadaş (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/friend-debug-interface-access-sdk.md)|Arkadaş sınıfları ve arkadaş işlevleri simgesi.|  
|[FunctionType](../../debugger/debug-interface-access/functiontype.md)|Her benzersiz işlev imzası simgesi.|  
|[FunctionArgType](../../debugger/debug-interface-access/functionargtype.md)|Her parametre için bir işlev simgesi.|  
|[VTableShape](../../debugger/debug-interface-access/vtableshape.md)|Sanal tablonun boyutunu simgesi.|  
|[VTable](../../debugger/debug-interface-access/vtable.md)|Sanal bir tablo simgesi.|  
|[CustomType](../../debugger/debug-interface-access/customtype.md)|Satıcı tanımlı bir tür simgesi.|  
|[ManagedType](../../debugger/debug-interface-access/managedtype.md)|Meta verilerde tanımlanan bir tür simgesi.|  
|[Boyut](../../debugger/debug-interface-access/dimension.md)|Dizi boyutları simgesi.|  
  
> [!NOTE]
>  Her simge, diğer sembol başvuruları yanı sıra sembol bilgilerini tutan özelliklere sahip olabilir. Bu özellikleri tek tek sembol konularında listelenmiştir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [CV_access_e numaralandırması](../../debugger/debug-interface-access/cv-access-e.md)   
 [Simge türlerinin sözcük hiyerarşisi](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [Simgeler ve Simge Etiketleri](../../debugger/debug-interface-access/symbols-and-symbol-tags.md)