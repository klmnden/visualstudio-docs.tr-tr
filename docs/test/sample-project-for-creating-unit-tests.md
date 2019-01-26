---
title: Birim testleri oluşturmak için örnek kod
description: Bu makalede, Visual Studio'da birim testleri test edilebilir örnek kodu sağlıyor.
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: sample
helpviewer_keywords:
- unit test sample [Visual Studio]
- unit tests, samples
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 172cf928c52f31f650337c5f0d449e28ccecc294
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55018533"
---
# <a name="sample-code-for-testing"></a>Test için örnek kod

Bu örnek kod içeren bir sınıf *BankAccount*, çeşitli yöntemlerle ile birim testleri test edilebilir.

Kod, aşağıdaki yönergelerde kullanılır:

- [Yönetilen kod için birim testleri oluşturma ve çalıştırma](../test/walkthrough-creating-and-running-unit-tests-for-managed-code.md). Bu izlenecek yol, oluşturma ve birim testlerini özelleştirme, bunları çalıştırmak ve test sonuçları inceleyin adımlarında size yol gösterir.
- [Komut satırı test yardımcı programını kullanarak](https://msdn.microsoft.com/Library/52c11992-9e94-4067-a4b7-59f19d69d867). Bu kılavuzda, kullandığınız *MSTest.exe* testleri çalıştırmak ve sonuçları görüntülemek için komut satırı yardımcı programı.

## <a name="sample-code"></a>Örnek kod

Bu örnekte yalnızca kasıtlı hata içinde banka yöntemi "m_balance += amount" bir artı eşittir işareti önce oturum eksi gerektiğidir.

```csharp
using System;

namespace BankAccountNS
{
    /// <summary>
    /// Bank Account demo class.
    /// </summary>
    public class BankAccount
    {
        private string m_customerName;

        private double m_balance;

        private bool m_frozen = false;

        private BankAccount()
        {
        }

        public BankAccount(string customerName, double balance)
        {
            m_customerName = customerName;
            m_balance = balance;
        }

        public string CustomerName
        {
            get { return m_customerName; }
        }

        public double Balance
        {
            get { return m_balance; }
        }

        public void Debit(double amount)
        {
            if (m_frozen)
            {
                throw new Exception("Account frozen");
            }

            if (amount > m_balance)
            {
                throw new ArgumentOutOfRangeException("amount");
            }

            if (amount < 0)
            {
                throw new ArgumentOutOfRangeException("amount");
            }

            m_balance += amount; // intentionally incorrect code
        }

        public void Credit(double amount)
        {
            if (m_frozen)
            {
                throw new Exception("Account frozen");
            }

            if (amount < 0)
            {
                throw new ArgumentOutOfRangeException("amount");
            }

            m_balance += amount;
        }

        private void FreezeAccount()
        {
            m_frozen = true;
        }

        private void UnfreezeAccount()
        {
            m_frozen = false;
        }

        public static void Main()
        {
            BankAccount ba = new BankAccount("Mr. Bryan Walton", 11.99);

            ba.Credit(5.77);
            ba.Debit(11.22);
            Console.WriteLine("Current balance is ${0}", ba.Balance);
        }
    }
}
```

/ * Örnek şirketler, kuruluşlar, ürünler, etki alanı adları, e-posta adresleri, logolar, kişiler, yerler ve sahiplerinin hayal ürünüdür. Gerçek şirket, kuruluş, ürün, etki alanı adı, e-posta adresi, logo, kişi, yer veya olayları ile hiçbir ilişki amaçlanmamıştır veya çıkarılmamalıdır. \*/

## <a name="create-the-project"></a>Projeyi oluşturma

Bu kod ile çalışmak için önce bir proje için Visual Studio içinde oluşturun. Projeyi oluşturmak için adımları [izlenecek yol: Yönetilen kod için birim testleri oluşturma ve çalıştırma](../test/walkthrough-creating-and-running-unit-tests-for-managed-code.md#create-a-project-to-test).

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: Yönetilen kod için birim testleri oluşturma ve çalıştırma](../test/walkthrough-creating-and-running-unit-tests-for-managed-code.md)
- [İzlenecek yol: Komut satırı test yardımcı programını kullanın](https://msdn.microsoft.com/Library/52c11992-9e94-4067-a4b7-59f19d69d867)
