---
title: EncUnavailableReason | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- EncUnavailableReason
helpviewer_keywords:
- EncUnavailableReason enumeration
ms.assetid: c10aa4c0-d7e0-4de1-b8ff-7e050985eb12
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b804ce1d7ada1de0c457662c93542b1e0fef996a
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49925701"
---
# <a name="encunavailablereason"></a>EncUnavailableReason
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

`This is for internal use only!` Nedenler temsil eder, **Düzenle ve devam et** kullanılabilir değil.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum tagEncUnavailableReason {  
   ENCUN_NONE,  
   ENCUN_INTEROP,  
   ENCUN_SQLCLR,  
   ENCUN_MINIDUMP,  
   ENCUN_EMBEDDED,  
   ENCUN_ATTACH,  
   ENCUN_WIN64  
};  
typedef enum tagEncUnavailableReason EncUnavailableReason;  
```  
  
```csharp  
public enum EncUnavailableReason {  
   ENCUN_NONE,  
   ENCUN_INTEROP,  
   ENCUN_SQLCLR,  
   ENCUN_MINIDUMP,  
   ENCUN_EMBEDDED,  
   ENCUN_ATTACH,  
   ENCUN_WIN64  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 ENCUN_NONE  
 Belirli neden neden Düzenle ve devam et kullanılabilir değil.  
  
 ENCUN_INTEROP  
 Düzenle ve devam et kullanılabilir değil bir birlikte çalışabilirlik çağrısı sırasında.  
  
 ENCUN_SQLCLR  
 Düzenle ve devam et kullanılabilir değil, ortak dil çalışma zamanı (CLR) kullanan bir SQL yordam çağrısı sırasında.  
  
 ENCUN_MINIDUMP  
 Düzenle ve devam et kullanılabilir değil bir mini döküm işlenirken.  
  
 ENCUN_EMBEDDED  
 Düzenle ve devam et kullanılamıyor katıştırılmış kod işlerken.  
  
 ENCUN_ATTACH  
 Düzenle ve devam et kullanılamıyor oturum iliştirilmiş olduğundan değil başlatıldığında hata ayıklayıcı tarafından.  
  
 ENCUN_WIN64  
 Düzenle ve devam et kullanılamıyor 64 bit Windows kod işlenirken.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu iç kullanım için yalnızca göre numaralandırmadır [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)]. [GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md) ve [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md) özel bağlantı noktası sağlayıcısı tarafından uygulanan yöntemleri her zaman döndürmelidir `E_NOTIMPL`.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.idl  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)   
 [GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md)

