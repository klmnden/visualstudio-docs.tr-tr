---
title: Numaralandırıcılar | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, enumerators
ms.assetid: a60030c5-e1d1-47e1-84bb-cbfe838ab479
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2d3a0876dfd3a9d7b9cc86b18f6e9a6ba3b780d3
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66334504"
---
# <a name="enumerators"></a>Numaralandırıcılar
Bu bölümde, kaynak denetimi eklentisi hakkında bilmeniz gereken kaynak denetimi eklentisi API Numaralandırıcı veri türlerini listeler.

## <a name="in-this-section"></a>Bu bölümde
- [Komut kodu](../extensibility/command-code-enumerator.md) seçeneklerini numaralandırır [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md) ve [SccPopulateList](../extensibility/sccpopulatelist-function.md) işlevleri.

- [İleti](../extensibility/message-enumerator.md) yazdırma geri çağırma için kullanılan bayrakları numaralandırır [LPTEXTOUTPROC](../extensibility/lptextoutproc.md).

- [Dosya durumu kod](../extensibility/file-status-code-enumerator.md) adlı kaynak denetimi altındaki bir dosyayı durumunu belirten sabit değerleri içerir.

- [Dizin durumu kod](../extensibility/directory-status-code-enumerator.md) adlı kaynak denetimi altında bir dizin durumunu belirten sabit değerleri içerir.

## <a name="related-sections"></a>İlgili bölümler
- [Kaynak Denetimi Eklentisi oluşturma](../extensibility/internals/creating-a-source-control-plug-in.md) kaynak denetimi eklentisi SDK tanımlar ve dahil edilen kaynaklar açıklanır.

- [SccGetCommandOptions](../extensibility/sccgetcommandoptions-function.md) verilen komutu için Gelişmiş Seçenekleri kullanıcıya sorar.

- [SccPopulateList](../extensibility/sccpopulatelist-function.md) bunların geçerli durum için dosyaların listesini inceler. Ayrıca, kullandığı `pfnPopulate` işlevi bir dosya için ölçüt eşleşmediğinde çağrıyı yapana bunu bildirmesi `nCommand`.

- [LPTEXTOUTPROC](../extensibility/lptextoutproc.md) açıklar tarafından kullanılan geri çağırma işlevi [SccOpenProject](../extensibility/sccopenproject-function.md) kaynak denetimi eklentisi IDE üzerinden alınan iletileri görüntülemek için.

- [Kaynak denetimi eklentileri](../extensibility/source-control-plug-ins.md) kaynak denetimi eklentisi API içindeki tüm öğelerin tam listesini sağlar.