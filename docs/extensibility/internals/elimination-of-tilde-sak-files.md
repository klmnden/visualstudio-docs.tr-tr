---
title: Saydamlığından ~ SAK dosyalarının | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- temporary files
- ~sak files
- source control plug-ins, ~SAK files
ms.assetid: 5277b5fa-073b-4bd1-8ba1-9dc913aa3c50
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 96704b52fb31085fad7546687a8803c85bcfbb47
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63418638"
---
# <a name="elimination-of-sak-files"></a>Saydamlığından ~ SAK dosyalarının
Kaynak Denetimi Eklentisi API 1.2 içindeki *~ SAK* özellik bayraklarının dosyalar değiştirildi ve bir kaynak olup olmadığını algılayan yeni işlevleri denetim eklentisini destekler *MSSCCPRJ* dosya ve paylaşımlı kullanıma Almalarla.

## <a name="sak-files"></a>~ SAK dosyalarının
Visual Studio .NET 2003 oluşturulan geçici dosyalar ön ekine sahip *~ SAK*. Bu dosyalar kaynak denetimi eklentisi destekleyip desteklemediğini belirlemek için kullanılır:

- *MSSCCPRJ.SCC* dosya.

- Birden çok (paylaşılan) kullanıma alma.

Kaynak Denetimi Eklentisi API 1.2 ile sağlanan gelişmiş işlevleri destekleyen eklentileri için yeni özellikler, bayraklar ve İşlevler, aşağıdaki bölümlerde ayrıntılı kullanımı geçici dosyalar oluşturmadan bu özellikler IDE algılayabilir.

## <a name="new-capability-flags"></a>Yeni özellik bayrakları
 `SCC_CAP_SCCFILE`

 `SCC_CAP_MULTICHECKOUT`

## <a name="new-functions"></a>Yeni işlevleri
- [SccWillCreateSccFile](../../extensibility/sccwillcreatesccfile-function.md)

- [SccIsMultiCheckoutEnabled](../../extensibility/sccismulticheckoutenabled-function.md)

 Kaynak Denetimi Eklentisi birden çok (paylaşılan) kullanıma destekler ve ardından bunu bildirir, `SCC_CAP_MULTICHECKOUT` yetenek ve uygular `SccIsMultiCheckOutEnabled` işlevi. Kaynak denetimli projelerin herhangi bir kullanıma alma işlemi oluştuğunda, bu işlev çağrılır.

 Kaynak Denetimi Eklentisi oluşturulmasını ve kullanılmasını desteklediği durumlarda bir *MSSCCPRJ.SCC* bildirir, sonra dosya `SCC_CAP_SCCFILE` yetenek ve uygular [SccWillCreateSccFile](../../extensibility/sccwillcreatesccfile-function.md). Bu işlev, dosyaların bir listesini çağrılır. İşlev döndürür `TRUE' or 'FALSE` Visual Studio kullanması gerekip gerekmediğini belirtmek her bir dosya için bir *MSSCCPRJ.SCC* dosyasının. Kaynak denetimi eklentisi şu yeni özellikleri ve işlevleri desteklemiyor seçerse bu dosyalarının oluşturulmasını devre dışı bırakmak için aşağıdaki kayıt defteri anahtarını kullanabilirsiniz:

 **[HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl] DoNotCreateTemporaryFilesInSourceControl** = *DWORD: 00000001*

> [!NOTE]
> Bu kayıt defteri anahtarı ayarlanırsa *DWORD: 00000000*, varolmayan olan anahtarına eşdeğerdir ve Visual Studio geçici dosyalar oluşturmak yine de çalışır. Ancak, kayıt defteri anahtarı ayarlanırsa *DWORD: 00000001*, geçici dosyalar oluşturmak Visual Studio denemez. Bunun yerine kaynak denetimi eklentisi desteklemediği varsayar *MSSCCPRJ.SCC* dosya ve paylaşımlı kullanıma Almalarla desteklemez.

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi API sürümü 1.2 yenilikler nelerdir?](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)