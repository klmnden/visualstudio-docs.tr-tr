---
title: IDE tarafından uygulanan geri çağırma işlevleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, callback functions
- callback functions, source control plug-ins
ms.assetid: 4a8833f0-6ac0-4ea7-9400-8275aa991468
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fc3b4423b54975c773de743b093f882f1fd9c42c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62926942"
---
# <a name="callback-functions-implemented-by-the-ide"></a>IDE tarafından uygulanan geri çağırma işlevleri
Bir birleşik son kullanıcı deneyimi sağlar ve mümkün olduğunca sorunsuz olarak tümleşik geliştirme ortamı (IDE) ile tümleştirme yapmak için kaynak denetimi eklentisi IDE tarafından uygulanan geri çağırma işlevleri kullanabilirsiniz. Eklenti bu işlevler IDE bilgi geçirmek için bir kaynak denetimi işlemi sırasında uygun zamanlarda çağırabilirsiniz; IDE, katıştırılmış öğeler kendi yerel kullanıcı Arabirimi olarak bu bilgiler daha sonra görüntüleyebilirsiniz. Kullanıcı, bu senaryoda, eklenti kendi UI işe, daha az parçalanmış bir deneyimi vardır.

 Gerekli bir üstbilgi dosyasıdır *scc.h*. Varsayılan konum *\Program Files\VSIP 8.0\EnvSDK\common\inc\\*. Ayrıca kaynak denetimi eklentisi örneğine sahip VSIP klasörde olduğu *\Program Files\VSIP 8.0\MSSCCI\\*.

## <a name="in-this-section"></a>Bu bölümde
- [LPTEXTOUTPROC](../extensibility/lptextoutproc.md) açıklar tarafından kullanılan geri çağırma işlevi [SccOpenProject](../extensibility/sccopenproject-function.md) kaynak denetimi eklentisi IDE üzerinden alınan iletileri görüntülemek için.

- [POPLISTFUNC](../extensibility/poplistfunc.md) açıklar tarafından kullanılan geri çağırma işlevi [SccPopulateList](../extensibility/sccpopulatelist-function.md) zaman IDE tam erişimi yok yalnızca kaynak denetimi eklentisi tam bir listesi gibi kullanılabilir olan bilgiler Sürüm denetimi altına dosya.

- [QUERYCHANGESFUNC](../extensibility/querychangesfunc.md) açıklar tarafından kullanılan geri çağırma işlevi [SccQueryChanges](../extensibility/sccquerychanges-function.md) işlemi.

- [POPDIRLISTFUNC](../extensibility/popdirlistfunc.md) açıklar tarafından kullanılan geri çağırma işlevi [SccPopulateDirList](../extensibility/sccpopulatedirlist-function.md) işlemi.

- [OPTNAMECHANGEPFN](../extensibility/optnamechangepfn.md) açıklar geri çağırma işlevine bir çağrı tarafından ayarlanan [SccSetOption](../extensibility/sccsetoption-function.md) kaynak denetimi Eklentisi adı değişiklikleri geri IDE'ye iletişim kurmasına olanak tanır.

## <a name="related-sections"></a>İlgili bölümler
- [SccOpenProject](../extensibility/sccopenproject-function.md) bir proje açılır.

- [SccPopulateList](../extensibility/sccpopulatelist-function.md) bunların geçerli durum için dosyaların listesini inceler. Ayrıca, kullandığı `pfnPopulate` işlevi bir dosya için ölçüt eşleşmediğinde çağrıyı yapana bunu bildirmesi `nCommand`.

- [SccPopulateDirList](../extensibility/sccpopulatedirlist-function.md) dizinleri ve dosyaları bir proje veya kaynak denetimi altında olan projeler listesini inceler. Bulunan her dizin ve dosya adı, bir geri çağırma işlevine geçirilir.

- [SccQueryChanges](../extensibility/sccquerychanges-function.md) dosyaların listesini yapılan ad değişiklikleri inceler. Her dosya adının, değişiklik durumuyla birlikte bir geri çağırma işlevine geçirilir.

- [SccSetOption](../extensibility/sccsetoption-function.md) çok çeşitli seçenekler ayarlar. Her seçeneği ile başlayan `SCC_OPT_xxx` ve kendi tanımlanan değerleri kümesi vardır.

- [Kaynak denetimi eklentileri](../extensibility/source-control-plug-ins.md) kaynak denetimi eklentisi SDK başvuru bölümü içeriğini açıklar.