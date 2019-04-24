---
title: Exibir itens selecionados no Explorer ativo
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b722bcb404f987a6f07a9fe305046ea6673dc231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356382"
---
# <a name="display-selected-items-in-the-active-explorer"></a>Exibir itens selecionados no Explorer ativo

Este exemplo mostra como usar a classe auxiliar OutlookItem para exibir convenientemente todos os itens escolhidos na janela ativa do Explorer.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O objeto [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) contém o conjunto de itens do Outlook atualmente escolhidos no explorador ativo do Outlook. Nem o explorador ativo, representado pelo [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), nem o conjunto de itens escolhidos indica o tipo dos itens escolhidos. Normalmente, você teria que primeiro identificar o tipo de item e, em seguida, chamar o método **Display** específico para esse tipo. Como o método **Display** é comum para todos os objetos de itens do Outlook e a classe auxiliar OutlookItem inclui esse método, aproveite a classe auxiliar declarando uma instância do objeto OutlookItem, myItem e utilize myItem.Display para exibir cada item na seleção. Você pode ver a implementação da classe auxiliar OutlookItem em [Criar uma classe auxiliar para acessar membros de itens comuns do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySelectedItems()
{
    Outlook.Selection selection =
        Application.ActiveExplorer().Selection;
    for (int i = 1; i <= selection.Count; i++)
    {
        OutlookItem myItem = new OutlookItem(selection[i]);
        myItem.Display();
    }
}
```

## <a name="see-also"></a>Confira também

- [Criar uma classe auxiliar para acessar membros comuns do item do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Itens gerais do Outlook](general-outlook-items.md)

