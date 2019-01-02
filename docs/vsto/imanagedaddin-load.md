---
title: IManagedAddin::Load
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords: ''
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 67a1f330862ad6156d85a8f86afcfe863d776850
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53924455"
---
# <a name="imanagedaddinload"></a>IManagedAddin::Load
  Yönetilen bir VSTO Eklenti yüklendiğinde çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```csharp
HRESULT Load([in] BSTR bstrManifestURL,   
             [in] IDispatch *pdispApplication);  
```  
  
### <a name="parameters"></a>Parametreler  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|*bstrManifestURL*|İçin VSTO eklentisi bildiriminin tam yolu.|  
|*pdispApplication*|VSTO eklentisi yükleniyor ana bilgisayar uygulaması temsil IDispatch yönelik işaretçi.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntemi başarıyla tamamlanıp tamamlanmadığını belirten bir HRESULT değer.  
  
## <a name="remarks"></a>Açıklamalar  
 VSTO eklentisi yükünü dengeleyebilmek için kullanılan bilgileri sağlayan bir dosya (genellikle, bir XML dosyası) bildirimidir. Örneğin, bir bildirim VSTO eklenti derlemesi ve giriş noktası sınıfını VSTO Eklenti yüklendiğinde örneklemek için konumu belirtebilirsiniz.  
  
 *BstrManifestURL* parametre değerini içeren `Manifest` altında girdisi **HKEY_CURRENT_USER\Software\Microsoft\Office\\_\<uygulama adı >_ \Addins\\_\<eklenti kimliği >_**  VSTO eklentisi için kayıt defteri anahtarı. Daha fazla bilgi için [Imanagedaddin arabirimi](../vsto/imanagedaddin-interface.md).  
  
 Uygulama [IManagedAddIn::Load](../vsto/imanagedaddin-load.md) VSTO yüklenmekte eklentisi için uygulama etki alanı ve güvenlik ilkesi yapılandırma gibi görevleri gerçekleştirmek için yöntemi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Imanagedaddin arabirimi](../vsto/imanagedaddin-interface.md)   
 [IManagedAddin::Unload](../vsto/imanagedaddin-unload.md)  
