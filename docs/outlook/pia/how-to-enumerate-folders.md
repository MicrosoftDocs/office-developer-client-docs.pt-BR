---
title: Enumerar pastas
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fe79f78ba1aab1e54df0b0bc88fa0c55c73e187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357397"
---
# <a name="enumerate-folders"></a>Enumerar pastas

Este exemplo mostra como enumerar pastas por iteração por meio de um conjunto de pastas.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

No exemplo código a seguir, o método EnumerateFoldersInDefaultStore primeiro obtém a pasta raiz do armazenamento padrão usando o método [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)). Ele chama o método EnumerateFolders na pasta raiz. EnumerateFolders assume uma pasta raiz e percorre as pastas do armazenamento padrão que representa a pasta raiz. EnumerateFolders primeiro usa a propriedade [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) para ter as subpastas do objeto raiz [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)). EnumerateFolders é então chamado recursivamente para enumerar todas as pastas em uma hierarquia. Por fim, EnumerateFolders grava a propriedade [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) de cada **Folder** para os ouvintes de rastreamento no conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a>Confira também

- [Pastas](folders.md)

