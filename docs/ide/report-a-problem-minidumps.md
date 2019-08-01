---
title: Tüm çağrı yığınları ile mini döküm oluşturma
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
ms.openlocfilehash: 7d0580e04968a01dc8e447a9ee35f2b1c5934ccf
ms.sourcegitcommit: 85d66dc9fea3fa49018263064876b15aeb6f9584
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "68461647"
---
# <a name="create-minidumps-for-a-visual-studio-process-with-all-call-stacks"></a>Tüm çağrı yığınlarıyla Visual Studio işlemi için mini döküm oluşturma

Bazı durumlarda Microsoft, çalışan bir Visual Studio işleminin tüm çağrı yığınları hakkında bilgi içeren bir mini döküm isteyebilir. Bu bilgileri toplamak için şu adımları uygulayın:

## <a name="create-the-minidump-file"></a>Mini döküm dosyası oluşturma

1. Visual Studio 'nun yeni bir örneğini başlatın.
1. Ana menüden,**işleme Ekle** **Hata Ayıkla** > ' yı seçin.
1. İlgili **yönetilen** ve **Yerel** onay kutularını işaretleyin ve **Ekle**'ye basın.

   ![İşleme İliştir](../ide/media/attach-to-process.png)

1. Çalışan işlemlerin listesinden iliştirilecek diğer Visual Studio örneğini seçin.
1. Ana menüden **Hata Ayıkla** > **Tümünü kes**' i seçin.
1. Ana menüden,**dökümü farklı kaydet kayıt** **Ayıkla** > ' yı seçin.

## <a name="get-the-call-stacks-from-the-minidump"></a>Mini döküm dosyasından çağrı yığınlarını al

1. Döküm dosyasını Visual Studio 'da açın.
1. **Araç**   seçenekleri hata ayıklamasimgeleriveMicrosoftsembolsunucularınınsemboldosyası(.pdb)konumlarındaişaretliolduğundaneminolun. >  >  > 
1. **Komut** penceresini açın (**diğer Windows** > **komut penceresini** **görüntüle** > )
1. ' ~ * K ' yazın. Pencerede tüm iş parçacıklarının çağrı yığınları görüntülenir.
1. Komut penceresinden tüm metni kopyalayın ve bir metin dosyasına kaydedin.
1. Txt dosyasını hataya iliştirin.
