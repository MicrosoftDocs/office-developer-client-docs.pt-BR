---
title: Exibir listas de endereços para um perfil
TOCTitle: Display the address lists for a profile
ms:assetid: ced8230b-110b-4ccb-a699-588798144154
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184643(v=office.15)
ms:contentKeyID: 55119802
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 9809603a7c54c9b1ce30c956ebef1a8fb9b6c208
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405942"
---
# <a name="display-the-address-lists-for-a-profile"></a>Exibir listas de endereços para um perfil

Este exemplo mostra como exibir listas de endereços para o perfil atual.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O perfil atual contém listas de endereços que são representadas pelo conjunto [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)). Para obter uma instância do conjunto AddressLists, você deve usar a propriedade [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).

No exemplo de código a seguir, EnumerateAddressLists primeiro enumera cada objeto [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) no conjunto AddressLists usando uma instrução foreach. O exemplo, em seguida, cria uma cadeia de caracteres que contém os valores das propriedades [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)) e [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)). Finalmente,EnumerateAddressLists escreve a cadeia de caracteres para rastrear ouvintes do conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx). São exibidas listas de endereços para o perfil atual.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAddressLists()
{
    Outlook.AddressLists addrLists =
         Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Display Name: " + addrList.Name);
        sb.AppendLine("Resolution Order: "
            + addrList.ResolutionOrder.ToString());
        sb.AppendLine("Read-only : "
            + addrList.IsReadOnly.ToString());
        sb.AppendLine("Initial Address List: "
            + addrList.IsInitialAddressList.ToString());
        sb.AppendLine("");
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>Confira também

- [Catálogo de endereços](address-book.md)

