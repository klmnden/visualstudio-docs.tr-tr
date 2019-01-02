---
title: DISASSEMBLY_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- DISASSEMBLY_FLAGS
helpviewer_keywords:
- DISASSEMBLY_FLAGS enumeration
ms.assetid: c1ec5a4d-5d42-4660-932c-7348550140cb
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7b0e4f793b0dcfe7a8a35bfeb06a3acd53c969d5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53961015"
---
# <a name="disassemblyflags"></a>DISASSEMBLY_FLAGS
Ayrıştırılmış kod bayrakları belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_DISASSEMBLY_FLAGS {   
   DF_DOCUMENTCHANGE     = 0x00000001,  
   DF_DISABLED           = 0x00000002,  
   DF_INSTRUCTION_ACTIVE = 0x00000004,  
   DF_DATA               = 0x00000008,  
   DF_HASSOURCE          = 0x00000010,  
   DF_DOCUMENT_CHECKSUM  = 0x00000020  
};  
typedef DWORD DISASSEMBLY_FLAGS;  
```  
  
```csharp  
public enum enum_DISASSEMBLY_FLAGS {   
   DF_DOCUMENTCHANGE     = 0x00000001,  
   DF_DISABLED           = 0x00000002,  
   DF_INSTRUCTION_ACTIVE = 0x00000004,  
   DF_DATA               = 0x00000008,  
   DF_HASSOURCE          = 0x00000010,  
   DF_DOCUMENT_CHECKSUM  = 0x00000020  
};  
```  
  
## <a name="members"></a>Üyeler  
 DF_DOCUMENTCHANGE  
 Bu yönerge önceki olandan farklı bir belge olduğunu gösterir.  
  
 DF_DISABLED  
 Bu yönerge yürütülmeyecek gösterir.  
  
 DF_INSTRUCTION_ACTIVE  
 Bu yönerge yürütülecek sonraki yönergeleri biri olduğunu gösterir (olabilir birden fazla).  
  
 DF_DATA  
 Bu yönerge gerçekten veri (kodunda değil) olduğunu gösterir.  
  
 DF_HASSOURCE  
 Bu yönerge kaynağına sahip olduğunu gösterir. Profil oluşturma ya da çöp toplama kod gibi bazı yönergeler, karşılık gelen hiçbir kaynak vardır.  
  
 DF_DOCUMENT_CHECKSUM  
 Bildiren `bstrDocumentUrl` alanı sonra belgesi URL'si sağlama toplamı veri içeriyor. İçin Açıklamalar bölümüne bakın [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) yapısı için sağlama toplamı veriler nasıl depolanır.  
  
## <a name="remarks"></a>Açıklamalar  
 Olarak kullanılan `dwFlags` üyesi [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) yapısı.  
  
 Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)