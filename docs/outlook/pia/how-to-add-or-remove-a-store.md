---
title: Adicionar ou remover um repositório
TOCTitle: Add or remove a store
ms:assetid: db2930ec-ef99-4e31-86c5-820e8368e05f
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612380(v=office.15)
ms:contentKeyID: 55119895
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4346f3bf1b7bba1f26a34e1562997b4d043c8d49
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723023"
---
# <a name="add-or-remove-a-store"></a>Adicionar ou remover um repositório

Este exemplo mostra como adicionar e remover um repositório em determinado perfil.

## <a name="example"></a>Exemplo

Este exemplo de código mostra como adicionar e remover um armazenamento em um perfil especificado, chamando o método [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) e o método [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)), respectivamente, no objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).

No Outlook, você pode adicionar ou remover um repositório PST somente por meio de programação. O exemplo de código a seguir adiciona um armazenamento Unicode e coloca o arquivo .pst no local padrão dos arquivos .pst do usuário: Documents and Settings\\\<UserName\>\\Local Settings\\Application Data\\Microsoft\\Outlook. O exemplo de código usa Environment.SpecialFolder.LocalApplicationData para recuperar o caminho para a pasta Application Data na pasta Local Settings. Depois que o repositório foi adicionado, o exemplo de código remove o repositório. Como o método **RemoveStore** requer um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) para remover o objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)), ele enumera a coleção [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) para localizar o objeto **Store** que acaba de ser adicionado com base na propriedade [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) do objeto **Store**.

**RemoveStore** remove apenas o repositório do perfil atual. Não exclui o arquivo .pst do sistema de arquivos.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateUnicodePST()
    Dim path As String = Environment.GetFolderPath( _
        Environment.SpecialFolder.LocalApplicationData) _
        & "\Microsoft\Outlook\MyUnicodeStore.pst"
    Try
        Application.Session.AddStoreEx( _
            path, Outlook.OlStoreType.olStoreUnicode)
        Dim stores As Outlook.Stores = Application.Session.Stores
        For Each store As Outlook.Store In stores
            If store.FilePath = path Then
                Dim folder As Outlook.Folder = _
                    CType(store.GetRootFolder(), Outlook.Folder)
                ' Remove the store
                Application.Session.RemoveStore(folder)
            End If
        Next
    Catch ex As Exception
        Debug.WriteLine(ex.Message)
    End Try
End Sub
```


```csharp
private void CreateUnicodePST()
{
    string path = Environment.GetFolderPath(
        Environment.SpecialFolder.LocalApplicationData)
        + @"\Microsoft\Outlook\MyUnicodeStore.pst";
    try
    {
        Application.Session.AddStoreEx(
            path, Outlook.OlStoreType.olStoreUnicode);
        Outlook.Stores stores = Application.Session.Stores;
        foreach (Outlook.Store store in stores)
        {
            if (store.FilePath == path)
            {
               Outlook.Folder folder =
                    store.GetRootFolder() as Outlook.Folder;
               // Remove the store
               Application.Session.RemoveStore(folder);
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a>Confira também

- [Repositórios](stores.md)

