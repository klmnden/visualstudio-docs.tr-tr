---
title: Kaynak denetimi bilgilerinin kaldırılması. Proj ve. Sln dosyaları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, .sln and .proj files
ms.assetid: 7b06883f-35de-41e2-9a9e-d3edba236f17
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1cd49b27804e35e28395c78a6e177db1461a54f4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54943376"
---
# <a name="removal-of-source-control-information-from-proj-and-sln-files"></a>.Proj ve .Sln Dosyalarından Kaynak Denetimi Bilgilerinin Kaldırılması
Kaynak Denetimi Eklentisi API SCC 1.2 sürümüne bilgiler bir MSSCCPRJ içinde depolanır. SCC dosyası. MSSCCPRJ yararlanın. SCC SCC bilgilerin olduğu değil kaynak - denetimli .proj ve .sln dosyalarında olduğu gibi dosyasıdır.  
  
## <a name="version-12-changes"></a>Sürüm 1.2  
 Kaynak denetimi kaynak denetimi eklentisi API sürüm 1.1 üzerinde alan eklentileri, kaynak denetimi ile ilgili bilgi (.proj) proje ve çözüm (.sln) dosyalarında depolanır. Kaynak denetimi bilgilerinin veritabanı konumu AuxPath tarafından belirlenir ve veritabanı içinde belirli bir konuma ProjName tarafından belirtilir. ProjName genellikle tüm bu işlemleri sonra geçersiz olacağından bu davranışı dal, çatal veya kopyalama işlemleri sonrasında sorunlara neden olabilir.  
  
 Kaynak Denetimi Eklentisi API kullanılan sürüm 1.1, IDE içinde ~ SAK dosyalarının bir eklenti MSSCCPRJ destekleyip desteklemediğini belirlemek için. Kaynak denetimi bilgilerinin depolanması SCC yöntemi. Kaynak Denetimi Eklentisi API sürümü 1.2 MSSCCPRJ desteği saptamak için yeni bir özellik sağlar. SCC dosyası kullanmadan bir ~ SAK dosya. Daha fazla bilgi için [Saydamlığından ~ SAK dosyalarının](../../extensibility/internals/elimination-of-tilde-sak-files.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API Sürümü 1.2’deki Yenilikler](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)