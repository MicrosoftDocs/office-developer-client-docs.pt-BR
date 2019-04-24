---
title: Criar um modo de exibição
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c91f43001d6c56ad3b4c316aede9845a5e0a0064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349487"
---
# <a name="create-a-view"></a>Criar um modo de exibição

Este exemplo mostra como usar o método [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) da coleção [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) para criar um modo de exibição para o objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho da [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Você pode criar modos de exibição personalizáveis que permitem que você classifique, agrupe e exiba dados de todos os tipo diferentes no Painel de Exibição da janela do explorador do Outlook. Você também pode personalizar modos de exibição internos de modo programático. A tabela a seguir lista os objetos que representam os modos de exibição do Outlook.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome do Objeto</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></p></td>
<td><p>Os dados são exibidos como uma série de imagens de cartões de visita eletrônicos.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></p></td>
<td><p>Os dados são exibidos no formato de calendário.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></p></td>
<td><p>Os dados são exibidos em uma série de cartões.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></p></td>
<td><p>Os dados são exibidos como ícones da pasta Windows ou ícones do explorador.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></p></td>
<td><p>Os dados são exibidos como uma tabela simples baseada em um campo.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></p></td>
<td><p>Os dados são exibidos em uma linha do tempo linear personalizável.</p></td>
</tr>
</tbody>
</table>


Você pode acessar métodos e propriedades que são comuns para todos os modos de exibição usando o objeto[View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)). Entretanto, para acessar certas propriedades que não são comuns para todos os modos de exibição, você deve converter o objeto **View** em um objeto **View** derivado ao qual pertence a propriedade que você quer acessar. Por exemplo, para acessar a propriedade [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) do objeto **Cardview**, converta o objeto **View** no objeto **Cardview**. Se você quiser determinar que tipo de modo de exibição é representado por um objeto **View** específico, use a propriedade [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)).

Para criar um novo modo de exibição, use o método **Add** da coleção **Views** para um objeto **Folder**. Em seguida, defina a visibilidade do modo de exibição no momento da criação ou a qualquer momento depois que o modo de exibição for criado. Para definir a visibilidade do modo de exibição no momento da criação, especifique uma constante [OIViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) no parâmetro *SaveOption* do método **Add**. Para definir a visibilidade a qualquer momento depois da criação do modo de exibição, especifique uma constante **OlViewSaveOption** para a propriedade [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) do objeto **View**. 

A adição de um novo modo de exibição gera o evento [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) evento da coleção **Views**. Após a criação do modo de exibição, personalize o modo de exibição programaticamente convertendo o objeto **View** em um dos objetos derivados e fazendo as alterações necessárias em seguida. Use o método **Save** do objeto derivado **View**, ou o objeto **View** para salvar quaisquer alterações no modo de exibição. Finalmente, use o método **Apply** do objeto derivado **View** ou o objeto **View** para aplicar o modo de exibição ao objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) atual. Isso gera o evento [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) do objeto **Explorer**.

O exemplo de código a seguir, CreateMeetingRequestsView, adiciona um novo modo de exibição chamado “Meeting Requests” à Caixa de Entrada do usuário gerando um objeto **View** para um objeto **TableView**. CreateMeetingRequestsView chama o método **Add** do objeto **Views** com o parâmetro *Name* definido para “Meeting Requests” e o parâmetro *ViewType* definido para **olTableView**. A propriedade [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) do objeto **TableView** é definida para uma cadeia de caracteres DAV Searching and Locating (DASL), que faz com que o modo de exibição exiba apenas quando houver itens que contêm “IPM.Schedule” na classe de mensagem do item. Então, o novo modo de exibição é salvo e aplicado.

Se você usar o Visual Studio para testar este exemplo de código, deve adicionar primeiro uma referência ao componente da Biblioteca de Objetos do Microsoft Outlook 15.0 e especificar a variável do Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateMeetingRequestsView()
{
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.Views views =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Views;
    Outlook.TableView tableView = (Outlook.TableView)
        views.Add("Meeting Requests",
        Outlook.OlViewType.olTableView,
        Outlook.OlViewSaveOption.olViewSaveOptionThisFolderEveryone);
    tableView.Filter = "\"" + PR_MESSAGE_CLASS + "\"" +
        " like 'IPM.Schedule%'";
    tableView.Save();
    tableView.Apply();
}
```

## <a name="see-also"></a>Confira também

- [Modos de exibição](views.md)

