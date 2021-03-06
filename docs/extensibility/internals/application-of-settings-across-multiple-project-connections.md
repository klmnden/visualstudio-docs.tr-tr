---
title: Birden çok proje bağlantısında ayarların uygulanması | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, application of settings
ms.assetid: 2116d3d0-c46c-4d0a-b482-08a178584f46
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 480ccaac58e67a959454e9d4afa9aa57e817c693
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66315838"
---
# <a name="application-of-settings-across-multiple-project-connections"></a>Birden çok proje bağlantısında ayarların uygulanması
Kaynak Denetimi Eklentisi Kaynak Denetimi Eklentisi API sürümü 1.2 kullanılarak oluşturulan bir toplu işlem birden fazla proje veya birden çok bağlantı bağlamları arasında aynı kaynak denetimi işlemi yürütmek için kullanabilirsiniz. Toplu kullanılabilir yedekli ortadan kaldırmak için proje başına kullanıcı deneyiminden iletişim kutuları.

 Bir kullanıcı birden fazla bağlantı kaynak denetimi eklentisi API sürüm 1.1 (örneğin, iki web projeleri farklı bir dosya paylaşımı makinelerde) kullanılarak oluşturulan bir kaynak denetimi eklentisi içinde ait birden çok öğe seçilir ve bunları denetler, kullanıcı aynı görür iletişim kutusunu tekrar tekrar. Kullanıcı olsa bile, bu senaryo ortaya **tümüne uygula** IDE her bağlantı bağlamı için durumuna sıfırlar çünkü iletişim kutusunda, kutuyu işaretleyin.

## <a name="new-capability-flag"></a>Yeni özellik bayrağı
 `SccBeginBatch` İşlev kümeleri `SCC_CAP_BATCH` toplu işlem sürmekte olduğunu belirten bayrak.

## <a name="new-functions"></a>Yeni işlevleri
Toplu işlem aşağıdaki yeni işlevleri destekler:

- [SccBeginBatch](../../extensibility/sccbeginbatch-function.md)

- [SccEndBatch](../../extensibility/sccendbatch-function.md)

`SCCBeginBatch` İşlevi, bir grup kaynak denetimi işlemleri başlatır. `SccEndBatch` İşlev grubu kapatır. Grupları bulunmayabilir.

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi API sürümü 1.2 yenilikler nelerdir?](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)