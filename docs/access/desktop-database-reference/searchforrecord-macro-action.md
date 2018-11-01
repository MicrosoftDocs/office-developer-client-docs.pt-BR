---
title: Ação da macro ProcurarRegistro
TOCTitle: SearchForRecord Macro Action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9bb498771e5a1ac3a8e6eb19b3b1ec2886867214
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876488"
---
# <a name="searchforrecord-macro-action"></a><span data-ttu-id="3453d-102">Ação da macro ProcurarRegistro</span><span class="sxs-lookup"><span data-stu-id="3453d-102">SearchForRecord Macro Action</span></span>


<span data-ttu-id="3453d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3453d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3453d-104">Você pode usar a ação **ProcurarRegistro** para procurar um registro em uma tabela, consulta, formulário ou relatório específico.</span><span class="sxs-lookup"><span data-stu-id="3453d-104">You can use the **SearchForRecord** action to search for a specific record in a table, query, form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="3453d-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="3453d-105">Setting</span></span>

<span data-ttu-id="3453d-106">A ação **ProcurarRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="3453d-106">The **SearchForRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3453d-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="3453d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3453d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3453d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3453d-109"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-p101">Digite ou selecione o tipo de objeto de banco de dados que você está procurando. É possível selecionar <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong> ou <strong>Relatório</strong>.</span><span class="sxs-lookup"><span data-stu-id="3453d-p101">Enter or select the type of database object that you are searching in. You can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, or <strong>Report</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3453d-112"><strong>Nome do Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-112"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-p102">Digite ou selecione o objeto específico que contenha o registro a ser pesquisado. A lista suspensa mostra todos os objetos de banco de dados do tipo selecionado pelo argumento <strong>Tipo de objeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="3453d-p102">Enter or select the specific object that contains the record to search for. The drop-down list shows all database objects of the type you selected for the <strong>Object Type</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3453d-115"><strong>Objeto Record</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-115"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-116">Especifique o ponto de início e a direção da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3453d-116">Specify the starting point and direction of the search.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3453d-117">Configuração</span><span class="sxs-lookup"><span data-stu-id="3453d-117">Setting</span></span></p></th>
<th><p><span data-ttu-id="3453d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="3453d-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3453d-119"><strong>Previous</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-119"><strong>Previous</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-120">Pesquisa registros anteriores ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="3453d-120">Search backward from the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3453d-121"><strong>Next</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-121"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-122">Pesquisa registros posteriores ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="3453d-122">Search forward from the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3453d-123"><strong>Primeira</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-123"><strong>First</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-p103">Pesquisa registros posteriores a partir do primeiro registro. Este é o valor padrão do argumento.</span><span class="sxs-lookup"><span data-stu-id="3453d-p103">Search forward from the first record. This is the default value for this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3453d-126"><strong>Último</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-126"><strong>Last</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-127">Pesquisa registros anteriores a partir do último registro.</span><span class="sxs-lookup"><span data-stu-id="3453d-127">Search backward from the last record.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3453d-128"><strong>Condição Onde</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-128"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-129">Insira os critérios para a pesquisa usando a mesma sintaxe como uma cláusula SQL WHERE, apenas sem a palavra &quot;onde&quot;.</span><span class="sxs-lookup"><span data-stu-id="3453d-129">Enter the criteria for the search using the same syntax as an SQL WHERE clause, only without the word &quot;WHERE&quot;.</span></span> <span data-ttu-id="3453d-130">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="3453d-130">For example,</span></span></p>
<p>`Description = "Beverages"`</p>
<p><span data-ttu-id="3453d-131">Para criar um critério que inclui um valor de uma caixa de texto em um formulário, você deve criar uma expressão que concatena a primeira parte do critério com o nome da caixa de texto que contém o valor a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="3453d-131">To create a criterion that includes a value from a text box on a form, you must create an expression that concatenates the first part of the criterion with the name of the text box containing the value for which to search.</span></span> <span data-ttu-id="3453d-132">Por exemplo, o seguinte critério pesquisará o campo Descrição para o valor na caixa de texto denominada Txtdescrição no formulário denominado frmCategories.</span><span class="sxs-lookup"><span data-stu-id="3453d-132">For example, the following criterion will search the Description field for the value in the text box named txtDescription on the form named frmCategories.</span></span> <span data-ttu-id="3453d-133">Observe o sinal de igualdade (<strong>=</strong>) no início da expressão e o uso de aspas simples (<strong>'</strong>) em ambos os lados da referência de caixa de texto:</span><span class="sxs-lookup"><span data-stu-id="3453d-133">Note the equal sign (<strong>=</strong>) at the beginning of the expression, and the use of single quotation marks (<strong>'</strong>) on either side of the text box reference:</span></span></p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3453d-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="3453d-134">Remarks</span></span>

- <span data-ttu-id="3453d-135">Quando mais de um registro satisfizer os critérios do argumento **CondiçãoOnde**, os seguintes fatores determinarão o registro a ser localizado:</span><span class="sxs-lookup"><span data-stu-id="3453d-135">In cases where more than one record matches the criteria in the **Where Condition** argument, the following factors determine which record is found:</span></span>
    
  - <span data-ttu-id="3453d-136">**Definição do argumento o registro** Consulte a tabela na seção configurações para obter mais informações sobre o argumento **registro** .</span><span class="sxs-lookup"><span data-stu-id="3453d-136">**The Record argument setting**See the table in the Settings section for more information about the **Record** argument.</span></span>
    
  - <span data-ttu-id="3453d-137">**A ordem de classificação dos registros** Por exemplo, se o argumento **registro** é definido como o **primeiro**, alterando a ordem de classificação dos registros pode alterar registro a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="3453d-137">**The sort order of the records**For example, if the **Record** argument is set to **First**, changing the sort order of the records might change which record is found.</span></span>

- <span data-ttu-id="3453d-p106">O objeto especificado no argumento **NomeDeObjeto** deve ser aberto antes da execução dessa ação. Caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="3453d-p106">The object specified in the **Object Name** argument must be open before this action is run. Otherwise, an error occurs.</span></span>

- <span data-ttu-id="3453d-140">Se os critérios do argumento **CondiçãoOnde** não forem satisfeitos, não ocorrerão erros e o foco permanecerá no registro atual.</span><span class="sxs-lookup"><span data-stu-id="3453d-140">If the criteria in the **Where Condition** argument are not met, no error occurs and the focus remains on the current record.</span></span>

- <span data-ttu-id="3453d-p107">Ao pesquisar o registro anterior ou o próximo, a pesquisa não será "concluída" quando alcançar o fim dos dados. Se não houver mais registros que atendam aos critérios, não ocorrerão erros e o foco permanecerá no registro atual. Para confirmar se uma correspondência foi encontrada, você pode inserir uma condição para a próxima ação e torná-la igual aos critérios do argumento **CondiçãoOnde**.</span><span class="sxs-lookup"><span data-stu-id="3453d-p107">When searching for the previous or next record, the search does not "wrap" when it reaches the end of the data. If there are no further records that match the criteria, no error occurs and the focus remains on the current record. To confirm that a match was found, you can enter a condition for the next action, and make the condition the same as the criteria in the **Where Condition** argument.</span></span>

- <span data-ttu-id="3453d-144">Para executar a ação **ProcurarRegistro** em um módulo do VBA, use o método **SearchForRecord** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="3453d-144">To run the **SearchForRecord** action in a VBA module, use the **SearchForRecord** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="3453d-p108">A ação **ProcurarRegistro** é semelhante à ação **[EncontrarRegistro](findrecord-macro-action.md)**, mas **ProcurarRegistro** tem recursos de pesquisa mais avançados. A ação **EncontrarRegistro** é usada principalmente para localizar cadeias de caracteres, e ela duplica a funcionalidade da caixa de diálogo **Localizar**. A ação **ProcurarRegistro** usa critérios que são mais parecidos com os de um filtro ou de uma consulta SQL. A lista a seguir demonstra alguns procedimentos que você pode executar com a ação **ProcurarRegistro**:</span><span class="sxs-lookup"><span data-stu-id="3453d-p108">The **SearchForRecord** action is similar to the **[FindRecord](findrecord-macro-action.md)** action, but **SearchForRecord** has more powerful search features. The **FindRecord** action is primarily used for finding strings, and it duplicates the functionality of the **Find** dialog box. The **SearchForRecord** action uses criteria that are more like those of a filter or an SQL query. The following list demonstrates some things you can do with the **SearchForRecord** action:</span></span>
    
  - <span data-ttu-id="3453d-149">É possível usar critérios complexos no argumento **CondiçãoOnde**; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3453d-149">You can use complex criteria in the **Where Condition** argument, such as</span></span>
        
    `Description = "Beverages" and CategoryID = 11`
    
  - <span data-ttu-id="3453d-150">É possível fazer referência a campos localizados na fonte de registros de um formulário ou relatório, mas que não são exibidos no formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="3453d-150">You can refer to fields that are in the record source of a form or report but aren't displayed on the form or report.</span></span> <span data-ttu-id="3453d-151">No exemplo anterior, nem descrição nem CategoryID deve ser exibido no formulário ou relatório para os critérios trabalhar.</span><span class="sxs-lookup"><span data-stu-id="3453d-151">In the preceding example, neither Description nor CategoryID must be displayed on the form or report for the criteria to work.</span></span>
    
  - <span data-ttu-id="3453d-p110">Você pode usar operadores lógicos, como **\<**, **\>**, **E**, **OU** e **ENTRE**. A ação **EncontrarRegistro** localiza somente cadeias de caracteres que sejam iguais a, comecem com ou contenham a cadeia pesquisada.</span><span class="sxs-lookup"><span data-stu-id="3453d-p110">You can use logical operators, such as **\<**, **\>**, **AND**, **OR**, and **BETWEEN**. The **FindRecord** action only matches strings that equal, start with, or contain the string being searched for.</span></span>

## <a name="example"></a><span data-ttu-id="3453d-154">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3453d-154">Example</span></span>

<span data-ttu-id="3453d-p111">Esta macro primeiro abre a tabela Categorias usando a ação **AbrirTabela**. A macro então usa a ação **ProcurarRegistro** para localizar o primeiro registro da tabela em que o campo Descrição é igual a "Bebidas".</span><span class="sxs-lookup"><span data-stu-id="3453d-p111">The following macro first opens the Categories table by using the **OpenTable** action. The macro then uses the **SearchForRecord** action to find the first record in the table where the Description field equals "Beverages."</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3453d-157">Ação</span><span class="sxs-lookup"><span data-stu-id="3453d-157">Action</span></span></p></th>
<th><p><span data-ttu-id="3453d-158">Argumentos</span><span class="sxs-lookup"><span data-stu-id="3453d-158">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3453d-159"><strong>OpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-159"><strong>OpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-160"><strong>Nome da tabela</strong>: categorias de<strong>modo de exibição</strong>: <strong>Modo DatasheetData</strong>: <strong>Editar</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-160"><strong>Table Name</strong>: Categories<strong>View</strong>: <strong>DatasheetData Mode</strong>: <strong>Edit</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3453d-161"><strong>SearchForRecord</strong></span><span class="sxs-lookup"><span data-stu-id="3453d-161"><strong>SearchForRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="3453d-162"><strong>Tipo de objeto</strong>: <strong>Nome TableObject</strong>: categorias de<strong>registro</strong>: <strong>FirstWhere condição</strong>: descrição = &quot;bebidas&quot;</span><span class="sxs-lookup"><span data-stu-id="3453d-162"><strong>Object Type</strong>: <strong>TableObject Name</strong>: Categories<strong>Record</strong>: <strong>FirstWhere Condition</strong>: Description = &quot;Beverages&quot;</span></span></p></td>
</tr>
</tbody>
</table>

