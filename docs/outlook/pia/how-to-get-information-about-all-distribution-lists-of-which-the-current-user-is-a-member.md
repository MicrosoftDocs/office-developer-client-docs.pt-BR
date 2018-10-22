---
title: Obter informações sobre todas as listas de distribuição das quais o usuário atual participa
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f98d7a338866624e67d745e66a66e864fb9bbf99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406761"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a>Obter informações sobre todas as listas de distribuição das quais o usuário atual participa

Este exemplo usa o método [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) para obter informações sobre todas as listas de distribuição das quais o usuário atual participa.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

No exemplo a seguir, GetCurrentUserMembership chama o método **GetMemberOfList** para obter um conjunto [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) para todas as listas de distribuição das quais o usuário do Exchange é membro. Se o usuário não for membro de nenhuma lista de distribuição, **GetMemberOfList** retornará um conjunto **AddressEntries** com uma contagem de zero. O usuário conectado deve estar online para que **GetMemberOfList** retorne um conjunto **AddressEntries**. Caso contrário, **GetMemberOfList** retornará uma referência nula. GetCurrentUserMembership usa o método [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)), que retorna o objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) atual para testar se o usuário está online. Depois que as entradas de endereço são obtidas, o exemplo grava informações sobre cada uma das listas de distribuição do usuário para os ouvintes de rastreamento do conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Usuários do Exchange](exchange-users.md)

