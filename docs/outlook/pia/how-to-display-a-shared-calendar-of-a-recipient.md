---
title: Exibir um calendário compartilhado de um destinatário
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9230a63af66e8143a7da488ce41dadafe359429
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709212"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a>Exibir um calendário compartilhado de um destinatário

Este exemplo mostra como exibir o calendário compartilhado de um destinatário usando os métodos [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) e [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)).

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Itens enviáveis, como objetos [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), sempre expõem a propriedade [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) que, por sua vez, permite acessar o conjunto [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) do item enviável. Para criar um objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) que não está associado ao conjunto **Recipients** de um item, use o método [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Em seguida, passe este objeto **Recipient** não associado para o método [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)), que retorna uma pasta compartilhada do Exchange. Você pode então abrir a pasta compartilhada do Exchange e exibir essa pasta em uma janela do navegador. GetSharedDefaultFolder é usado nos cenários de representante do Exchange, onde o representante tem permissão para acessara pasta do delegante. Antes de passar o objeto **Recipient** para o método GetSharedDefaultFolder, você deve resolvê-lo. Para resolver um objeto **Recipient**, ligue para seu método [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)).

No exemplo código a seguir, DisplayManagerCalendar abre e exibe a pasta Calendário do gerente do usuário atual chamando **CreateRecipient** e **GetSharedDefaultFolder**. Uma caixa de diálogo de alerta é exibida se o usuário não tiver permissão para abrir a pasta Calendário do gerenciador ou se ocorrer um erro.


> [!NOTE]
> Quando você cria um objeto **Recipient** usando o método **CreateRecipient** do objeto **Namespace** ou o método [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) do conjunto **Recipients**, você deve fornecer um nome de destinatário. O **Recipient** é resolvido em relação a esse nome. Um nome de destinatário pode ter qualquer um dos seguintes formatos:
> - Nome para exibição
> - Alias
> - Endereço SMTP

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. O ** que usa a instrução** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayManagerCalendar()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.Recipient recip =
                Application.Session.CreateRecipient(manager.Name);
            if (recip.Resolve())
            {
                try
                {
                    Outlook.Folder folder =
                        Application.Session.GetSharedDefaultFolder(
                        recip, Outlook.OlDefaultFolders.olFolderCalendar)
                        as Outlook.Folder;
                    folder.Display();
                }
                catch
                {
                    MessageBox.Show("Could not open manager's calendar.",
                        "GetSharedDefaultFolder Example",
                        MessageBoxButtons.OK,
                        MessageBoxIcon.Error);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Calendar](calendar.md)

