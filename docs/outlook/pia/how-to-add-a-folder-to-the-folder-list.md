---
title: Adicionar uma pasta à lista de pastas
TOCTitle: Add a folder to the folder list
ms:assetid: f636a190-d966-4421-9977-0ead2bff5eee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184655(v=office.15)
ms:contentKeyID: 55119850
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dc8ead207261cfd4835e230981d923211771de7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405522"
---
# <a name="add-a-folder-to-the-folder-list"></a>Adicionar uma pasta à lista de pastas

Este exemplo mostra como usar o método [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) para adicionar uma pasta à lista de pastas do Outlook.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


No seguinte exemplo de código, **AddMyNewFolder** chama o método **Add** da coleção [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) para adicionar um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) que representa uma pasta chamada "Minha Nova Pasta" à lista de pastas **Inbox** do Outlook. "Minha Nova Pasta" é exibida.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. A seguinte linha de código mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddMyNewFolder()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Folders folders = folder.Folders;
    try
    {
        Outlook.Folder newFolder = folders.Add(
            "My New Folder", Type.Missing)
            as Outlook.Folder;
        newFolder.Display();
    }
    catch
    {
        MessageBox.Show(
            "Could not add 'My New Folder'",
            "Add Folder",
            MessageBoxButtons.OK,
            MessageBoxIcon.Error);
    }
}
```

## <a name="see-also"></a>Confira também

- [Pastas](folders.md)

