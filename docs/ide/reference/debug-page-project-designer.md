---
title: Hata Ayıklama Sayfası, Proje Tasarımcısı
ms.date: 06/27/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- vb.ProjectPropertiesDebug
helpviewer_keywords:
- Project Designer, Debug page
- Debug page in Project Designer
ms.assetid: ef11eae9-df96-4e20-aabd-2678ba317140
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c7b79b5aa5054781813d561089dab204bd1763bf
ms.sourcegitcommit: 935e341a02dba1c2aa3b6e89469388aa6e626f7f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53684768"
---
# <a name="debug-page-project-designer"></a>Hata Ayıklama Sayfası, Proje Tasarımcısı

Kullanım **hata ayıklama** sayfasının **Proje Tasarımcısı** davranışı Visual Basic veya C# projesinde hata ayıklama özelliklerini ayarlamak için.

Erişim için **hata ayıklama** sayfasında, içinde bir proje düğümü seçin **Çözüm Gezgini**. Üzerinde **proje** menüsünde seçin  **\<ProjectName > Özellikleri**. Zaman **Proje Tasarımcısı** görünen tıklayın **hata ayıklama** sekmesi.

> [!NOTE]
> Bu konu, UWP uygulamaları için geçerli değil. Bkz: [hata ayıklama oturumu başlatma (VB, C#, C++ ve XAML)](../../debugger/start-a-debugging-session-for-a-store-app-in-visual-studio-vb-csharp-cpp-and-xaml.md) UWP uygulamaları için.

## <a name="configuration-and-platform"></a>Yapılandırma ve Platform

Aşağıdaki seçenekler, görüntülenecek veya değiştirilecek platform ve yapılandırmayı seçmenize olanak sağlar.

**Yapılandırma**

Hangi yapılandırma ayarlarının görüntüleneceğini veya değiştirileceğini belirtir. Ayarları **hata ayıklama** (varsayılan), **yayın**, veya **yapılandırmalarında**.

**Platform**

Platform ayarlarının görüntüleneceğini veya değiştirileceğini belirtir. Seçimleri içerebilir **herhangi bir CPU** (varsayılan), **x64**, ve **x86**.

## <a name="start-action"></a>Başlatma eylemi

**Başlangıç eylemi** uygulamanın hataları ayıklanırken başlatılacak öğe belirtir: Proje, özel bir program, bir URL veya hiçbir şey. Varsayılan olarak, bu seçeneği ayarlamak **başlangıç projesi**. **Başlatma eylemi** ayarını **hata ayıklama** sayfa değerini belirler `StartAction` özelliği.

**Projeyi Başlat**

Yürütülebilir dosyası (Windows uygulaması ve konsol uygulaması projeleri) uygulamanın hataları ayıklanırken başlatılacak belirtmek için bu seçeneği belirleyin. Bu seçenek varsayılan olarak seçilidir.

**Harici program Başlat**

Uygulamanın hataları ayıklanırken belirli bir programı başlaması gerektiğini belirtmek için bu seçeneği belirleyin.

**Tarayıcı URL'si ile başlayın**

Uygulamanın hataları ayıklanırken belirli bir URL erişilmesi gerektiğini belirtmek için bu seçeneği belirleyin.

## <a name="start-options"></a>Başlatma seçenekleri

**Komut satırı bağımsız değişkenleri**

Bu metin kutusunda, hata ayıklama için kullanılacak komut satırı bağımsız değişkenleri girin.

**Çalışma dizini**

Bu metin kutusunda, projeyi başlatılacak dizini girin. Veya Gözat düğmesine tıklayın (**...** ) için bir dizin seçin.

**Uzak makine kullanma**

Uzak bir bilgisayardan bir uygulamada hata ayıklamak için bu onay kutusunu seçin ve metin kutusunda bir uzak bilgisayara yolunu girin.

## <a name="debugger-engines"></a>Hata ayıklayıcı altyapıları

**Yerel kod hata ayıklamayı etkinleştir**

Bu seçenek yerel kodun Hata Ayıklamasının desteklenip desteklenmediğini belirtir. COM nesneleri çağrıları yapıyorsanız veya projenizi çağıran ve yerel kodda yazılmış özel bir program başlatma ve yerel kod hata ayıklama, bu onay kutusunu işaretleyin. Yönetilmeyen kodun hata ayıklamasını devre dışı bırakmak için bu onay kutusunu temizleyin. Bu onay kutusu varsayılan olarak işaretli değildir.

**SQL Server hata ayıklamayı etkinleştir**

Seçin veya etkinleştirin veya Visual Basic uygulamanızdan SQL yordamlarının hata ayıklama devre dışı bırakmak için bu onay kutusunu temizleyin. Bu onay kutusu varsayılan olarak işaretli değildir.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio’da hata ayıklama](../../debugger/debugger-feature-tour.md)
- [C# Hata Ayıklama Yapılandırması Proje Ayarları](../../debugger/project-settings-for-csharp-debug-configurations.md)
- [Visual Basic Hata Ayıklama Yapılandırması Proje Ayarları](../../debugger/project-settings-for-a-visual-basic-debug-configuration.md)
- [Nasıl yapılır: Sınırlı izinler ile ClickOnce uygulamasında hata ayıklama](../../deployment/how-to-debug-a-clickonce-application-with-restricted-permissions.md)
- [Nasıl yapılır: Yapılandırmaları oluşturma ve düzenleme](../../ide/how-to-create-and-edit-configurations.md)