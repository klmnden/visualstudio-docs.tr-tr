---
title: VsgDbg sınıfı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 6722263c-ccef-40c7-a0ae-87a863fbab00
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 053647d48324f056148375bae9268b997ba8721f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801292"
---
# <a name="vsgdbg-class"></a>VsgDbg Sınıfı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Grafik tanılama uygulama bileşeninin programlı denetim için bir arabirimi temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
class VsgDbg;  
```  
  
## <a name="members"></a>Üyeler  
 `VsgDbg` Sınıfı aşağıdaki üyelere destekler.  
  
### <a name="public-constructors"></a>Ortak Oluşturucular  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[VsgDbg::VsgDbg (Oluşturucu)](../debugger/vsgdbg-vsgdbg-constructor.md)|Örneği oluşturur `VsgDbg` sınıfı ve isteğe bağlı olarak etkin bir şekilde yakalayıp grafik bilgilerini kaydetmek için grafik tanılama uygulama bileşeninin hazırlar.|  
|[VsgDbg::~VsgDbg (Yok Edici)](../debugger/vsgdbg-tilde-vsgdbg-destructor.md)|Örneğini yok eder `VsgDbg` sınıfı.|  
  
### <a name="public-methods"></a>Ortak Yöntemler  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[AddMessage](../debugger/addmessage.md)|Grafik tanılama baş üstü (baş yukarı görüntüleme) için özel bir ileti ekler.|  
|[BeginCapture](../debugger/begincapture.md)|İle biten bir yakalama aralık başlar `EndCapture`.|  
|[CaptureCurrentFrame](../debugger/capturecurrentframe.md)|Geçerli kare grafik günlük dosyasına geri kalanında yakalar.|  
|[Kopyalama (Programlı Yakalama)](../debugger/copy-programmatic-capture.md)|Etkin bir grafik günlüğü (.vsglog) dosyasının içeriğini yeni bir dosyaya kopyalar.|  
|[EndCapture](../debugger/endcapture.md)|İle başlatılan bir yakalama zaman aralığı sona `BeginCapture`.|  
|[Init](../debugger/init.md)|Etkin bir şekilde yakalayıp grafik bilgilerini kaydetmek için grafik tanılama uygulama bileşeninin hazırlar.|  
|[ToggleHUD](../debugger/togglehud.md)|Grafik tanılama baş üstü katmana açıp değiştirir.|  
|[UnInit](../debugger/uninit.md)|Grafik günlük dosyasını sonlandırır kapatılır ve uygulama, etkin bir şekilde grafik bilgilerini kaydetme sırasında kullanılan kaynakları serbest bırakır.|  
  
## <a name="remarks"></a>Açıklamalar  
 `VsgDbg` Sınıfı, grafik tanılama özelliklerine program aracılığıyla denetlemek için kullanabileceğiniz bir arabirimi temsil eder. Bazı özellikler bile, aktif yakalama ve grafik bilgilerini kaydetme kullanabilirsiniz; Bu içerir `AddMessage` üye işlevi ve `ToggleHUD` üye işlevi. Diğer üye işlevlerini başlatmak veya durdurmak etkin grafik bilgilerini yakalama için grafik tanılama uygulama bileşeninin hazırlama veya uygulamayı etkin bir şekilde yakalama ve grafik bilgilerini bir grafik günlük dosyasına kaydını çağrılmalıdır.
