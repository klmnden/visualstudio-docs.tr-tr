---
title: Mini döküm dosyalarında tüm çağrı yığınları ile oluşturma
ms.date: 06/27/2019
ms.topic: conceptual
helpviewer_keywords:
- minidumps for Visual Studio issues"
author: mikeblome
ms.author: mblome
manager: jillfra
dev_langs:
- CSharp
- VB
- CPP
ms.workload:
- multiple
ms.description: Collect minidumps to send to Microsoft for help with troubleshooting issues with Visual Studio
ms.openlocfilehash: eefcbefa8b728afa677e7bd04fd538633ae117f0
ms.sourcegitcommit: 6f7a740750b2cd17ea2275c3d046caebc9782917
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67518234"
---
# <a name="create-minidumps-for-a-visual-studio-process-with-all-call-stacks"></a>Mini döküm dosyalarında bir Visual Studio işlemi tüm çağrı yığınları ile oluşturma

Bazı durumlarda Microsoft, tüm çağrı yığınları için bilgi ile çalışan bir Visual Studio işlemi için bir mini döküm isteyebilir. Bu bilgileri toplamak için aşağıdaki adımları gerçekleştirin:

## <a name="create-the-minidump-file"></a>Mini döküm dosyası oluşturma

1. Visual Studio'nun yeni bir örneğini başlatın.
1. Ana menüden **hata ayıklama** > **İliştir**.
1. İlgili kontrol **yönetilen** ve **yerel** onay kutularını ve ENTER tuşuna **iliştirme**.

   ![İşleme](../ide/media/attach-to-process.png)

1. Diğer Visual Studio örneğinde çalışan işlemlerin listeden eklemek için seçin.
1. Ana menüden **hata ayıklama** > **tümünü Kes**.
1. Ana menüden **hata ayıklama** > **dökümü Farklı Kaydet**.

## <a name="get-the-call-stacks-from-the-minidump"></a>Çağrı yığınları mini döküm Al

1. Döküm dosyasını Visual Studio'da açın.

1. İçin alındı **Araçları** > **seçenekleri** > **hata ayıklama** > **sembolleri** ve o eminolun **Microsoft sembol sunucuları** iade **sembol dosyası (.pdb) konumlar**.
1. Açık **komut** penceresi (**görünümü** > **diğer Windows** > **komut penceresi**)
1. Türü ' ~ * k'. Tüm diziler çağrı yığınlarını pencere görüntüler.
1. Komut penceresinden bütün metni kopyalayın ve bir metin dosyasına kaydedin.
1. Txt dosyası hataya ekleyecek.
