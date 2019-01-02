---
title: API Başvurusu (Visual Studio hata ayıklama) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], API reference
ms.assetid: e4e429da-3667-41f7-9158-a8207d13e91a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 0172f9412bff791ae2446d6cffcd9d302c7c3ef8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53923633"
---
# <a name="api-reference-visual-studio-debugging"></a>API Başvurusu (Visual Studio Hata Ayıklama)
Başvuru bölümünde, API, sözdizimi ve kullanımı için tüm API öğeleri gösteren bir kılavuz kavramsal bir genel bakış ve kod örnekleri kaynaklardan içerir. Tüm başvurular, kategoriye göre alfabetik olarak listelenir.  
  
 Aşağıdaki tablo ortak gösterir `HRESULT` yöntemleri tarafından döndürülen değer.  
  
|Ad|Açıklama|Değer|  
|----------|-----------------|-----------|  
|S_OK|Başarılı.|0x00000000|  
|E_UNEXPECTED|Beklenmeyen hata oluştu.|0x8000FFFF|  
|E_NOTIMPL|Henüz uygulanmadı.|0x80004001|  
|E_OUTOFMEMORY|İşlemi tamamlamak için yeterli bellek yok.|0x8007000E|  
|E_INVALIDARG|Bir veya daha fazla bağımsız değişken geçersiz.|0x80070057|  
|E_NOINTERFACE|Böyle bir arabirim desteklenmiyor.|0x80004002|  
|E_POINTER|Geçersiz işaretçi.|0x80004003|  
|E_HANDLE|Geçersiz işleyici.|0x80070006|  
|E_ABORT|İşlem iptal edildi.|0x80004004|  
|E_FAIL|Beklenmeyen hata oluştu.|0x80004005|  
|E_ACCESSDENIED|Genel erişim reddedildi hatası.|0x80070005|  
  
> [!NOTE]
>  Olduğunda bir [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] yöntemi hata ayıklama döndürür `S_OK`, varsayılır parametresi işaretçiler geçerli olan her şeyi, diğer bir deyişle, doğrulama üzerinde parametresi işaretçileri yürütülür, `S_OK` döndürülür.  
> 
> [!NOTE]
>  Geçersiz veya `NULL` [out] parametreleri IDE'nin kilitlenmesine neden.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arabirimleri](../../../extensibility/debugger/reference/interfaces-visual-studio-debugging.md)   
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [Hata ayıklama için SDK Yardımcıları](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md)   
 [Visual Studio Hata Ayıklayıcı Genişletilebilirliği](../../../extensibility/debugger/visual-studio-debugger-extensibility.md)