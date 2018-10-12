---
title: SccCloseProject işlevi | Microsoft Docs
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
- SccCloseProject
helpviewer_keywords:
- SccCloseProject function
ms.assetid: 259c2069-d349-4814-810f-1c3151b7fb84
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 06f4e1e4ed8d59ce040c9bcfb531d16908d26c43
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49290790"
---
# <a name="scccloseproject-function"></a>SccCloseProject İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev, belirli bir oturum sonunu işaretlemek için bir proje, kapatır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
SCCRTN SccCloseProject (  
   LPVOID pvContext  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pvContext  
 Kaynak Denetimi Eklentisi bağlam yapısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Proje başarıyla kapatıldı.|  
|SCC_E_PROJNOTOPEN|Proje şu anda açıktır.|  
|SCC_E_NOTAUTHORIZED|Kullanıcı bu işlemi gerçekleştirmek için izin verilmiyor.|  
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata oluştu.|  
  
## <a name="remarks"></a>Açıklamalar  
 [SccOpenProject](../extensibility/sccopenproject-function.md) her zaman önce bu işlev çağrılır. Bu işlev çağrısı öğelerine yönelik çağrıdan sonra takip `SccOpenProject` işlevi veya [SccUninitialize](../extensibility/sccuninitialize-function.md), sona erdiği kaynak denetim sistemi bağlantısı tamamen.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [SccOpenProject](../extensibility/sccopenproject-function.md)   
 [SccInitialize](../extensibility/sccinitialize-function.md)

