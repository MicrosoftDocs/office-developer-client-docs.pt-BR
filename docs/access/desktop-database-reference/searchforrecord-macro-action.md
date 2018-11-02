---
title: Ação da macro ProcurarRegistro
TOCTitle: SearchForRecord macro action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 26a0a9fe66fb726bb728872ee31771d12b262864
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923696"
---
# <a name="searchforrecord-macro-action"></a>Ação da macro ProcurarRegistro


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **ProcurarRegistro** para procurar um registro em uma tabela, consulta, formulário ou relatório específico.

## <a name="setting"></a>Configuração

A ação **ProcurarRegistro** tem os seguintes argumentos.

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
<td><p><strong>Tipo de Objeto</strong></p></td>
<td><p>Digite ou selecione o tipo de objeto de banco de dados que você está procurando. É possível selecionar <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong> ou <strong>Relatório</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Objeto</strong></p></td>
<td><p>Digite ou selecione o objeto específico que contenha o registro a ser pesquisado. A lista suspensa mostra todos os objetos de banco de dados do tipo selecionado pelo argumento <strong>Tipo de objeto</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Objeto Record</strong></p></td>
<td><p>Especifique o ponto de início e a direção da pesquisa.</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuração</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Previous</strong></p></td>
<td><p>Pesquisa registros anteriores ao registro atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>Next</strong></p></td>
<td><p>Pesquisa registros posteriores ao registro atual.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Primeira</strong></p></td>
<td><p>Pesquisa registros posteriores a partir do primeiro registro. Este é o valor padrão do argumento.</p></td>
</tr>
<tr class="even">
<td><p><strong>Último</strong></p></td>
<td><p>Pesquisa registros anteriores a partir do último registro.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><strong>Condição Onde</strong></p></td>
<td><p>Insira os critérios para a pesquisa usando a mesma sintaxe como uma cláusula SQL WHERE, apenas sem a palavra &quot;onde&quot;. Por exemplo,</p>
<p>`Description = "Beverages"`</p>
<p>Para criar um critério que inclui um valor de uma caixa de texto em um formulário, você deve criar uma expressão que concatena a primeira parte do critério com o nome da caixa de texto que contém o valor a ser procurado. Por exemplo, o seguinte critério pesquisará o campo Descrição para o valor na caixa de texto denominada Txtdescrição no formulário denominado frmCategories. Observe o sinal de igualdade (<strong>=</strong>) no início da expressão e o uso de aspas simples (<strong>'</strong>) em ambos os lados da referência de caixa de texto:</p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

- Quando mais de um registro satisfizer os critérios do argumento **CondiçãoOnde**, os seguintes fatores determinarão o registro a ser localizado:
    
  - **Definição do argumento o registro** Consulte a tabela na seção configurações para obter mais informações sobre o argumento **registro** .
    
  - **A ordem de classificação dos registros** Por exemplo, se o argumento **registro** é definido como o **primeiro**, alterando a ordem de classificação dos registros pode alterar registro a ser localizado.

- O objeto especificado no argumento **NomeDeObjeto** deve ser aberto antes da execução dessa ação. Caso contrário, ocorrerá um erro.

- Se os critérios do argumento **CondiçãoOnde** não forem satisfeitos, não ocorrerão erros e o foco permanecerá no registro atual.

- Ao pesquisar o registro anterior ou o próximo, a pesquisa não será "concluída" quando alcançar o fim dos dados. Se não houver mais registros que atendam aos critérios, não ocorrerão erros e o foco permanecerá no registro atual. Para confirmar se uma correspondência foi encontrada, você pode inserir uma condição para a próxima ação e torná-la igual aos critérios do argumento **CondiçãoOnde**.

- Para executar a ação **ProcurarRegistro** em um módulo do VBA, use o método **SearchForRecord** do objeto **DoCmd**.

- A ação **ProcurarRegistro** é semelhante à ação **[EncontrarRegistro](findrecord-macro-action.md)**, mas **ProcurarRegistro** tem recursos de pesquisa mais avançados. A ação **EncontrarRegistro** é usada principalmente para localizar cadeias de caracteres, e ela duplica a funcionalidade da caixa de diálogo **Localizar**. A ação **ProcurarRegistro** usa critérios que são mais parecidos com os de um filtro ou de uma consulta SQL. A lista a seguir demonstra alguns procedimentos que você pode executar com a ação **ProcurarRegistro**:
    
  - É possível usar critérios complexos no argumento **CondiçãoOnde**; por exemplo:
        
    `Description = "Beverages" and CategoryID = 11`
    
  - É possível fazer referência a campos localizados na fonte de registros de um formulário ou relatório, mas que não são exibidos no formulário ou relatório. No exemplo anterior, nem descrição nem CategoryID deve ser exibido no formulário ou relatório para os critérios trabalhar.
    
  - Você pode usar operadores lógicos, como **\<**, **\>**, **E**, **OU** e **ENTRE**. A ação **EncontrarRegistro** localiza somente cadeias de caracteres que sejam iguais a, comecem com ou contenham a cadeia pesquisada.

## <a name="example"></a>Exemplo

Esta macro primeiro abre a tabela Categorias usando a ação **AbrirTabela**. A macro então usa a ação **ProcurarRegistro** para localizar o primeiro registro da tabela em que o campo Descrição é igual a "Bebidas".

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ação</p></th>
<th><p>Argumentos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>OpenTable</strong></p></td>
<td><p><strong>Nome da tabela</strong>: categorias de<strong>modo de exibição</strong>: <strong>Modo DatasheetData</strong>: <strong>Editar</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>SearchForRecord</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>Nome TableObject</strong>: categorias de<strong>registro</strong>: <strong>FirstWhere condição</strong>: descrição = &quot;bebidas&quot;</p></td>
</tr>
</tbody>
</table>

