---
title: VsgDbg sınıfı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 6722263c-ccef-40c7-a0ae-87a863fbab00
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4051a02de6a046621e62c21b4d2399b5a2703cb8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62895198"
---
# <a name="vsgdbg-class"></a>VsgDbg Sınıfı
Grafik tanılama uygulama bileşeninin programlı denetim için bir arabirimi temsil eder.

## <a name="syntax"></a>Sözdizimi

```C++
class VsgDbg;
```

## <a name="members"></a>Üyeler
 `VsgDbg` Sınıfı aşağıdaki üyelere destekler.

### <a name="public-constructors"></a>Ortak Oluşturucular

|Ad|Açıklama|
|----------|-----------------|
|[VsgDbg::VsgDbg (Oluşturucu)](vsgdbg-vsgdbg-constructor.md)|Örneği oluşturur `VsgDbg` sınıfı ve isteğe bağlı olarak etkin bir şekilde yakalayıp grafik bilgilerini kaydetmek için grafik tanılama uygulama bileşeninin hazırlar.|
|[VsgDbg::~VsgDbg (Yok Edici)](vsgdbg-tilde-vsgdbg-destructor.md)|Örneğini yok eder `VsgDbg` sınıfı.|

### <a name="public-methods"></a>Ortak Yöntemler

|Ad|Açıklama|
|----------|-----------------|
|[AddMessage](addmessage.md)|Grafik tanılama baş üstü (baş yukarı görüntüleme) için özel bir ileti ekler.|
|[BeginCapture](begincapture.md)|İle biten bir yakalama aralık başlar `EndCapture`.|
|[CaptureCurrentFrame](capturecurrentframe.md)|Geçerli kare grafik günlük dosyasına geri kalanında yakalar.|
|[Kopyalama (Programlı Yakalama)](copy-programmatic-capture.md)|Etkin bir grafik günlüğü (.vsglog) dosyasının içeriğini yeni bir dosyaya kopyalar.|
|[EndCapture](endcapture.md)|İle başlatılan bir yakalama zaman aralığı sona `BeginCapture`.|
|[Init](init.md)|Etkin bir şekilde yakalayıp grafik bilgilerini kaydetmek için grafik tanılama uygulama bileşeninin hazırlar.|
|[ToggleHUD](togglehud.md)|Grafik tanılama baş üstü katmana açıp değiştirir.|
|[UnInit](uninit.md)|Grafik günlük dosyasını sonlandırır kapatılır ve uygulama, etkin bir şekilde grafik bilgilerini kaydetme sırasında kullanılan kaynakları serbest bırakır.|

## <a name="remarks"></a>Açıklamalar
 `VsgDbg` Sınıfı, grafik tanılama özelliklerine program aracılığıyla denetlemek için kullanabileceğiniz bir arabirimi temsil eder. Bazı özellikler bile, aktif yakalama ve grafik bilgilerini kaydetme kullanabilirsiniz; Bu içerir `AddMessage` üye işlevi ve `ToggleHUD` üye işlevi. Diğer üye işlevlerini başlatmak veya durdurmak etkin grafik bilgilerini yakalama için grafik tanılama uygulama bileşeninin hazırlama veya uygulamayı etkin bir şekilde yakalama ve grafik bilgilerini bir grafik günlük dosyasına kaydını çağrılmalıdır.