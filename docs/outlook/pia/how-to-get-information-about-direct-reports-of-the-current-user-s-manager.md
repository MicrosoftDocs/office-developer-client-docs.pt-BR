---
title: 'Obter informações sobre subordinados diretos do gerente do usuário atual '
TOCTitle: Get information about direct reports of the current user's manager
ms:assetid: 768bf573-1b10-4776-8947-a7f8dc3ebde0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184617(v=office.15)
ms:contentKeyID: 55119842
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d49e96138d8cd2d857c49cc293258e1493afc747
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705572"
---
# <a name="get-information-about-direct-reports-of-the-current-users-manager"></a>Obter informações sobre subordinados diretos do gerente do usuário atual 

Este exemplo recebe os subordinados diretos do gerente atual do usuário, se houver algum, e exibe informações sobre cada um deles.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

No exemplo a seguir, o procedimento GetManagerDirectReports chama o método [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para obter o gerente do usuário, representado por um objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)). Se o usuário atual tiver um gerente, [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) será chamado para retornar um conjunto [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) que representa as entradas de endereço de todos os subordinados diretos do gerente do usuário. Se o gerente não tiver subordinados diretos, **GetDirectReports** retornará um conjunto **AddressEntries** com uma contagem de zero. Depois que os subordinados diretos do gerente forem obtidos, GetManagerDirectReports gravará informações sobre cada um deles para os ouvintes de rastreamento do conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).


> [!NOTE]
> O usuário conectado deve estar online para que esse método retorne um conjunto **AddressEntries**. Caso contrário, **GetDirectReports** retornará uma referência nula. No caso do código de produção, teste se o usuário está offline usando a propriedade [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) ou a propriedade [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) para vários cenários do Exchange.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerDirectReports()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.AddressEntries addrEntries =
                manager.GetDirectReports();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Outlook.ExchangeUser exchUser =
                        addrEntry.GetExchangeUser();
                    StringBuilder sb = new StringBuilder();
                    sb.AppendLine("Name: "
                        + exchUser.Name);
                    sb.AppendLine("Title: "
                        + exchUser.JobTitle);
                    sb.AppendLine("Department: "
                        + exchUser.Department);
                    sb.AppendLine("Location: "
                        + exchUser.OfficeLocation);
                    Debug.WriteLine(sb.ToString());
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Usuários do Exchange](exchange-users.md)

