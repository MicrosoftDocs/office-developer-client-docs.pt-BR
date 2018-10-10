---
title: Ação de macro DefinirClassificadoPor
TOCTitle: SetOrderBy Macro Action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3f14ea2fb2c41058fe15764c3f06931ffd0dc9ae
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464223"
---
# <a name="setorderby-macro-action"></a><span data-ttu-id="4973d-102">Ação de macro DefinirClassificadoPor</span><span class="sxs-lookup"><span data-stu-id="4973d-102">SetOrderBy Macro Action</span></span>


<span data-ttu-id="4973d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4973d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4973d-104">Você pode usar a ação **DefinirClassificadoPor** para especificar como deseja classificar os registros em um formulário, relatório, tabela ou resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="4973d-104">You can use the **SetOrderBy** action to specify how you want to sort records in a form, report, table, or query result.</span></span>

## <a name="setting"></a><span data-ttu-id="4973d-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="4973d-105">Setting</span></span>

<span data-ttu-id="4973d-106">A ação **DefinirClassificadoPor** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4973d-106">The **SetOrderBy** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4973d-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="4973d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4973d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4973d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4973d-109"><strong>Classificado Por</strong></span><span class="sxs-lookup"><span data-stu-id="4973d-109"><strong>Order By</strong></span></span></p></td>
<td><p><span data-ttu-id="4973d-110">Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais.</span><span class="sxs-lookup"><span data-stu-id="4973d-110">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4973d-111"><strong>Nome do Controle</strong></span><span class="sxs-lookup"><span data-stu-id="4973d-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4973d-p101">Se for fornecido e um objeto ativo for um formulário ou um relatório, o nome do controle que corresponde ao subformulário ou ao subrelatório a ser filtrado. Se estiver em branco e o objeto ativo for um formulário ou um relatório, o formulário ou relatório pai será classificado.</span><span class="sxs-lookup"><span data-stu-id="4973d-p101">If provided and the active object is a form or report, the name of the control that corresponds to the subform or subreport that will be sorted. If empty and the active object is a form or report, the parent form or report is sorted..</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4973d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4973d-114">Remarks</span></span>

<span data-ttu-id="4973d-115">Quando você executar essa ação de macro, a classificação será aplicada à tabela, ao formulário, ao relatório ou à folha de dados (resultado da pesquisa) que está ativa e que tem o foco.</span><span class="sxs-lookup"><span data-stu-id="4973d-115">When you run this macro action, the sort is applied to the table, form, report or datasheet (query result) that is active and has the focus.</span></span>

<span data-ttu-id="4973d-p102">O argumento Classificado Por é o nome do campo ou dos campos nos quais você deseja classificar registros. Quando você usa mais de um nome de campo, separe-os com vírgula (,). A propriedade **OrderBy** do objeto ativo é usada para salvar um valor de classificação e aplicá-lo posteriormente. Os valores de OrderBy são salvos com os objetos nos quais foram criados. Eles são carregados automaticamente quando o objeto é aberto, mas não são aplicados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4973d-p102">The Order By argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). The **OrderBy** property of the active object is used to save the ordering value and apply it at a later time. OrderBy values are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they aren't automatically applied.</span></span>

<span data-ttu-id="4973d-121">Quando você define o argumento Classificado Por digitando um ou mais nomes de campo e executa a macro, os registros são classificados por padrão em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="4973d-121">When you set the Order By argument by entering one or more field names and then run the macro, the records are sorted by default in ascending order.</span></span>

<span data-ttu-id="4973d-p103">Para classificar registros em ordem decrescente, digite DESC no final da expressão de argumento Classificado Por. Por exemplo, para classificar registros de cliente em ordem decrescente por nome de contato, defina o argumento OrderBy como "NomedoContato DESC". Para classificar nomes por Sobrenomes em ordem decrescente e Nomes em ordem crescente, defina o argumento Classificado Por como "Sobrenome DESC, Nome ASC".</span><span class="sxs-lookup"><span data-stu-id="4973d-p103">To sort records in descending order, type DESC at the end of the Order By argument expression. For example, to sort customer records in descending order by contact name, set the Order By argument to "ContactName DESC". To sort names by LastName descending, and FirstName ascending, set the Order By argument to "LastName DESC, FirstName ASC".</span></span>

