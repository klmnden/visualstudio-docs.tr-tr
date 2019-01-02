---
title: Sınıf Görünümü ve Nesne Tarayıcısı Simgeleri
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- icons, in Object Browser
- signal icons
- Class View tool, symbols
- graphic symbols
- IntelliSense, icons
- icons, IntelliSense
- symbols, Object Browser icons
- Object Browser, icons in Class View
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 29d39c210a14934ba50ace92692bee944b6b75c0
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53844398"
---
# <a name="class-view-and-object-browser-icons"></a>Sınıf Görünümü ve Nesne Tarayıcısı simgeleri

**Sınıf Görünümü** ve **Nesne Tarayıcısı** kod varlıklar, örneğin temsil eden simgeler, ad alanları, sınıflar, İşlevler ve değişkenler görüntüler. Aşağıdaki tabloda gösterilmiştir ve simgeleri açıklar.

|Simge|Açıklama|Simge|Açıklama|
|----------|-----------------|----------|-----------------|
|![Namespace simgesi](../ide/media/vxnamespace_icon.gif)|Ad Alanı|![Bildirim simgesi](../ide/media/vxmethod_icon.gif)|Yöntem veya işlev|
|![Sınıf simgesi](../ide/media/vxclass_icon.gif)|örneği|![İşleç simgesi](../ide/media/vxoperator_icon.gif)|İşleç|
|![Lolipop arabirimini sembolü](../ide/media/vxinterface_icon.gif)|Arabirim|![Özellik simgesi](../ide/media/vxproperty_icon.gif)|Özellik|
|![Yapı simgesi](../ide/media/vxstruct_icon.gif)|Yapı|![Alan simgesi](../ide/media/vxfield_icon.gif)|Alan veya değişken|
|![Birleşim simgesi](../ide/media/vxunion_icon.gif)|UNION|![Olay simgesi](../ide/media/vxevent_icon.gif)|Olay|
|![Sabit listesi simgesi](../ide/media/vxenum_icon.gif)|Enum|![Sabit simgesi](../ide/media/vxconstant_icon.gif)|Sabit|
|![Tür tanımı simgesi](../ide/media/vxtypedef_icon.gif)|Tür tanımı|![Öğe numaralandırma sembolü](../ide/media/vxenumitem_icon.gif)|Sabit listesi öğesi|
|![Visual Studio modülü simgesi](../ide/media/vxmodule_icon.gif)|Modül|![Eşleme öğesi simgesi](../ide/media/vxmapitem_icon.gif)|Eşleme öğesi|
|![Uzantı yöntemi simgesi](../ide/media/extensionmethod.gif)|Genişletme yöntemi|![Bildirim simgesi](../ide/media/vxmethod_icon.gif)|Dış bildirimi|
|![Temsilci simgesi](../ide/media/vxdelegate_icon.gif)|Temsilci|![Sınıf Görünümü ve nesne tarayıcısı hata simgesi](../ide/media/erroricon.gif)|Hata|
|![Özel durum simgesi](../ide/media/vxexception_icon.gif)|Özel Durum|![Şablon simgesi](../ide/media/vxtemplate_icon.gif)|Şablon|
|![Harita simgesi](../ide/media/vxmap_icon.gif)|Eşleme|![Hata ünlem işareti sembolü](../ide/media/vxerror_icon.gif)|Bilinmiyor|
|![Tür iletme simgesi](../ide/media/ob_type_forward.gif)|Tür iletme|||

## <a name="signal-icons"></a>Sinyal simgeleri

Aşağıdaki sinyal simgeleri, önceki tüm simgeleri uygulamak ve kendi erişilebilirlik gösterir.

|Simge|Açıklama|
|----------|-----------------|
|\<Sinyal simge yok >|Ortak alan. Erişilebilir herhangi bir yere bu bileşeni ve başvurduğu herhangi bir bileşeni.|
|![Sembol sinyal korumalı](../ide/media/vxsignal_icon_key.gif)|Korumalı. Kapsayan sınıfı türü veya bunları içeren sınıfı veya türü türetilmiş erişilebilir.|
|![Sinyal özel simge](../ide/media/vxsignal_icon_lock.gif)|Özel. Yalnızca kapsayan sınıfı veya türü içinde erişilebilir.|
|![Sembol korumalı sinyali](../ide/media/vxsignal_icon_envelope.gif)|Korumalı.|
|![Sinyal arkadaş&#47;iç simgesi](../ide/media/vxsignal_icon_diamond.gif)|İç arkadaş /. Yalnızca proje erişilebilir.|
|![Sinyal simgesi oku](../ide/media/vxsignal_icon_arrow.gif)|Kısayol. Nesne için bir kısayol.|

> [!NOTE]
> Projenize bir kaynak denetim veritabanında yer alıyorsa ek sinyal simgeleri kaynak denetimi durumunu belirtmek için görüntülenen, gibi iade veya olabilir kullanıma alındı.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod yapısını görüntüleme](../ide/viewing-the-structure-of-code.md)