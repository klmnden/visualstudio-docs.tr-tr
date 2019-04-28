---
title: Android hata ayıklayıcıyı özellikleri (C++) | Microsoft Docs
ms.custom: ''
ms.date: 10/23/2017
ms.technology: vs-ide-mobile
ms.topic: conceptual
ms.assetid: 789f7a1c-38b4-41d0-809b-14f4d96c8116
author: corob
ms.author: mblome
manager: jillfra
f1_keywords:
- VC.Project.AndroidDebugger.DebuggerType
- VC.Project.AndroidDebugger.AndroidDeviceID
- VC.Project.AndroidDebugger.PackagePath
- VC.Project.AndroidDebugger.LaunchActivity
ms.workload:
- xplat-cplusplus
ms.openlocfilehash: 9a4d7baa970008c2de7a3bc28966f7edbad68b21
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62819509"
---
# <a name="android-debugger-properties"></a>Android hata ayıklayıcıyı özellikleri

Özellik | Açıklama | Seçenekleri
--- | ---| ---
Hata ayıklayıcı türü | Hata ayıklanacak kod türlerini belirtir. | **Yalnızca yerel**<br>**Yalnızca Java**<br>
Hedef hata ayıklama | Hata ayıklama için kullanılacak öykünücüyü veya cihazı belirtir. Hiçbir öykünücü çalışmıyorsa, 'Android sanal cihazı (AVD) Manager' Lütfen kullanan bir cihazı başlatmak için.
Başlatılacak paket | Konumunu belirtir *.apk* , hataları ayıklanabilir. Uygulamanın hataları ayıklanırken belirli paketin (APK) başlatılmasını belirtmek için bu seçeneği belirleyin.
Başlatma etkinliği | Uygulamayı başlatmak için kullanılacak Android etkinliği, bildirimde kullanılan kimliğin eşleşmesi gerekir. Listeden almak için Uygula'ya basın *AndroidManifest.xml* ve dinamik olarak doldurma.
Ek sembol arama yolları | Hata ayıklama sembolleri için ek arama yolu.
Ek Java kaynağı arama yolları | Java kaynak dosyaları için ek arama yolları. (Yalnızca hata ayıklayıcı türü yalnızca Java olduğunda geçerlidir.)
