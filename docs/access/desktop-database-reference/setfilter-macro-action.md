---
title: Ação de macro DefinirFiltro
TOCTitle: SetFilter Macro Action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4292ded0638e8dbe3ad56aa835caa9c6541f0432
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874311"
---
# <a name="setfilter-macro-action"></a>Ação de macro DefinirFiltro

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **DefinirFiltro** para aplicar um filtro aos registros na folha de dados, formulário, relatório ou tabela ativa.

## <a name="setting"></a>Configuração

A ação **DefinirFiltro** tem os seguintes argumentos.

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
<td><p>Nome do Filtro</p></td>
<td><p>Se for fornecido, o nome de uma consulta ou de um filtro salvo como consulta. Este argumento ou o argumento WhereCondition é necessário em um banco de dados do cliente. Um banco de dados da web, esse argumento não está disponível.</p></td>
</tr>
<tr class="even">
<td><p>Condição Where</p></td>
<td><p>Se for fornecido, uma cláusula SQL WHERE que restringe os registros na folha de dados, formulário, relatório ou tabela. Um banco de dados da web, este argumento será necessário.</p></td>
</tr>
<tr class="odd">
<td><p>Nome do Controle</p></td>
<td><p>Se for fornecido, o nome do controle que corresponde ao subformulário ou ao subrelatório a ser filtrado. Se estiver em branco, o objeto atual será filtrado.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Em um banco de dados da Web, o argumento Condição Where não pode começar por um sinal de igualdade (=).

Quando você executar essa ação, o filtro será aplicado à tabela, ao formulário, ao relatório ou à folha de dados (por exemplo, resultado da pesquisa) que está ativa e que tem o foco.

A propriedade **Filtro** do objeto ativo é usada para salvar o argumento CondiçãoWhere e aplicá-lo posteriormente. Os filtros são salvos com os objetos nos quais foram criados. Eles são automaticamente carregados quando o objeto é aberto, mas não são automaticamente aplicados.

Em um banco de dados cliente, para aplicar um filtro automaticamente quando o objeto é aberto, defina a propriedade como **FiltrarNoCarregamento** com o valor True.

Em um banco de dados da Web, para aplicar um filtro automaticamente quando o objeto é aberto, adicione a ação **DefinirFiltro** a uma macro e adicione a macro ao evento **OnLoad** do objeto.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a ação Definirfiltro para filtrar o formulário no qual a macro é definida.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
