---
title: Obter informações sobre repositórios em um perfil
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0229294cd6655f9017780ee0d9a7a23de76f2362
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406565"
---
# <a name="get-information-about-stores-in-a-profile"></a>Obter informações sobre repositórios em um perfil

Este exemplo mostra como acessar e enumerar repositórios em um perfil.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Você pode usar o conjunto [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) para enumerar os repositórios de um determinado perfil. O conjunto **Stores** disponibiliza membros que expõem informações sobre cada objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)), como quando um objeto **Store** é adicionado ou quando um objeto **Store** está prestes a ser removido no perfil atual. No exemplo de código a seguir, EnumerateStores recebe o objeto **Stores** que representa repositórios no perfil atual e enumera esses repositórios. EnumerateStores examina cada objeto **Store** no conjunto **Stores**. Se a propriedade [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) retornar **true**, indicando que é um repositório .pst ou .ost, as propriedades [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) e [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) serão gravadas para os ouvintes de rastreamento no conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateStores()
{
    Outlook.Stores stores = Application.Session.Stores;
    foreach (Outlook.Store store in stores)
    {
        if (store.IsDataFileStore == true)
        {
            Debug.WriteLine(String.Format("Store: "
            + store.DisplayName
            + "\n" + "File Path: "
            + store.FilePath + "\n"));
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Repositórios](stores.md)

