---
title: Ação da macro ImportarListadoSharePoint
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291856"
---
# <a name="importsharepointlist-macro-action"></a>Ação da macro ImportarListadoSharePoint

**Aplica-se ao:** Access 2013, Office 2013

É possível usar a ação **ImportarListadoSharePoint** para importar ou vincular dados de um site do Microsoft SharePoint Foundation.

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável. 

## <a name="setting"></a>Setting

A ação **ImportarListadoSharePoint** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Tipo de transferência</strong></p></td>
<td><p>Selecione o tipo de transferência.</p>
<ul>
<li><p>Selecione <strong>Importar</strong> para copiar os dados do SharePoint Foundation para uma tabela no Microsoft Access. As atualizações nos dados no Access não afetam os dados no SharePoint Foundation. Da mesma forma, as atualizações dos dados no SharePoint Foundation não afetam os dados no Access.</p></li>
<li><p>Selecione <strong>Link</strong> para criar uma tabela vinculada no Access vinculada aos dados no SharePoint Foundation. As atualizações dos dados no Access são refletidas no SharePoint Foundation. Da mesma forma, as atualizações dos dados no SharePoint Foundation são refletidas no Access.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Endereço do site</strong></p></td>
<td><p>Digite o caminho completo do site do SharePoint.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ID da lista</strong></p></td>
<td><p>Digite o nome ou o GUID da lista a ser transferida. Argumento necessário.</p></td>
</tr>
<tr class="even">
<td><p><strong>ID do modo de exibição</strong></p></td>
<td><p>Digite o GUID do modo de exibição para a lista que deseja usar. Deixe este argumento em branco para transferir todas as linhas e colunas da lista.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nome da Tabela</strong></p></td>
<td><p>Digite o nome a ser exibido da tabela ou da tabela vinculada no Access.</p></td>
</tr>
<tr class="even">
<td><p><strong>Obter valores de exibição da pesquisa</strong></p></td>
<td><p>Selecione <strong>Sim</strong> para transferir valores de exibição para os campos Pesquisa, em vez da ID usada para executar a pesquisa.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

- Esta ação tem o mesmo efeito de clicar em **Lista do SharePoint** no grupo **Importar** da guia **Dados Externos**. Os argumentos da ação correspondem às escolhas feitas no Assistente para Obter Dados Externos.

- Para executar a ação **ImportarListadoSharePoint** em um módulo do VBA, use o método **TrasnferirListadoSharePoint** do objeto **DoCmd**.

- Se você especificar uma lista ou um modo de exibição inexistente, nenhum erro ocorrerá e nenhum dado será transferido.

- Um GUID é um identificador hexadecimal exclusivo de uma lista ou de um modo de exibição. Um GUID deve ser inserido no formato a seguir, em que cada "F" é um número hexadecimal (0 a 9 ou A a F).
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  Você pode obter o GUID de uma lista ou de um modo de exibição no site do SharePoint usando o seguinte procedimento:
    
  1. Abra a lista no SharePoint Foundation.
    
  2. Se o modo de exibição desejado não for exibido, clique na seta suspensa **Modo de Exibição** e selecione o modo de exibição desejado.
    
  3. Clique na seta suspensa **Modo de Exibição** e selecione **Modificar este Modo de Exibição**.O endereço na barra de endereços do navegador contém os GUIDs da lista e do modo de exibição. O GUID da lista vem depois de **List=** e o do modo de exibição, depois de **View=**. No entanto, no endereço, cada caractere **{** (chave esquerda) é representado pela cadeia de caracteres **%7B**, cada caractere **-** (hífen) é representado pela cadeia de caracteres **%2D** e cada caractere **}** (chave direita) é representado pela cadeia de caracteres **%7D**. Por exemplo:
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  Antes de poder usar os GUIDs do endereço como argumentos nesta ação de macro, você deve substituir cada cadeia de caracteres **%7B** pelo **caractere {,** substituir cada cadeia de caracteres **%2D** pelo caractere e substituir cada cadeia de caracteres **-** **%7D** pelo **caractere }.** Não inclua o caractere **&** (E comercial) que vem depois da cadeia de caracteres **%7D** no GUID da lista.

