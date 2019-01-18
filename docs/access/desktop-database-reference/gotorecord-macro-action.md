---
title: Ação da macro IrParaRegistro
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708477"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="9f3d8-102">Ação da macro IrParaRegistro</span><span class="sxs-lookup"><span data-stu-id="9f3d8-102">GoToRecord macro action</span></span>


<span data-ttu-id="9f3d8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f3d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f3d8-104">Você pode usar a ação **IrParaRegistro** para tornar o registro especificado no registro atual de um conjunto de resultados de tabela, formulário, ou consulta aberta.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="9f3d8-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="9f3d8-105">Setting</span></span>

<span data-ttu-id="9f3d8-106">A ação **IrParaRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f3d8-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="9f3d8-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9f3d8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f3d8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f3d8-109"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="9f3d8-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="9f3d8-p101">O tipo de objeto que contém o registro que você deseja tornar no atual. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Deixe este argumento em branco para selecionar o objeto ativo.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-p101">The type of object that contains the record you want to make current. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f3d8-113"><strong>Nome do Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="9f3d8-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9f3d8-p102">O nome do objeto que contém o registro que você deseja tornar no registro atual. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados atual do tipo selecionado pelo argumento <strong>Tipo de Objeto</strong>. Se você deixar o argumento <strong>Tipo de Objeto</strong> em branco, deixe este argumento em branco também.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-p102">The name of the object that contains the record you want to make the current record. The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f3d8-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="9f3d8-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="9f3d8-p103">O registro que se tornará o atual. Clique em <strong>Anterior</strong>, <strong>Próximo</strong>, <strong>Primeiro</strong>, <strong>Último</strong>, <strong>Ir Para</strong> ou <strong>Novo</strong> na caixa <strong>Registro</strong>. O padrão é <strong>Não</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-p103">The record to make the current record. Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box. The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f3d8-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="9f3d8-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="9f3d8-122">Um inteiro ou uma expressão que é avaliada como um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="9f3d8-123">Uma expressão deve ser precedida por um sinal de igualdade (<strong>=</strong>).</span><span class="sxs-lookup"><span data-stu-id="9f3d8-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="9f3d8-124">Este argumento especificará o registro para tornar o registro atual.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="9f3d8-125">Você pode usar o argumento <strong>deslocamento</strong> de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="9f3d8-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="9f3d8-126">Quando o argumento <strong>Registro</strong> é <strong>Próximo</strong> ou <strong>Anterior</strong>, o Microsoft Office Access 2007 move para frente ou para trás o número de registros especificado no argumento <strong>Deslocamento</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="9f3d8-p105">Quando o argumento <strong>Registro</strong> é <strong>Ir Para</strong>, o Access se move para o registro com o número igual ao do argumento <strong>Deslocamento</strong>. O número de registros é mostrado na caixa de número de registros na parte inferior da janela.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-p105">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p>
<p><span data-ttu-id="9f3d8-129"><strong>Observação</strong>: se você usar o <strong>primeiro</strong>, <strong>último</strong>ou <strong>novo</strong> a definição do argumento <strong>registro</strong> , o Access ignora o argumento <strong>deslocamento</strong> .</span><span class="sxs-lookup"><span data-stu-id="9f3d8-129"><strong>NOTE</strong>: If you use the <strong>First</strong>, <strong>Last</strong>, or <strong>New</strong> setting for the <strong>Record</strong> argument, Access ignores the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="9f3d8-130">Se você inserir um argumento <strong>deslocamento</strong> muito grande, o Access exibe uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-130">If you enter an <strong>Offset</strong> argument that is too large, Access displays an error message.</span></span> <span data-ttu-id="9f3d8-131">Você não pode inserir números negativos para o argumento <strong>deslocamento</strong> .</span><span class="sxs-lookup"><span data-stu-id="9f3d8-131">You can't enter negative numbers for the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="9f3d8-132">Quando o argumento <strong>Registro</strong> é <strong>Próximo</strong> ou <strong>Anterior</strong>, o Microsoft Office Access 2007 move para frente ou para trás o número de registros especificado no argumento <strong>Deslocamento</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="9f3d8-p107">Quando o argumento <strong>Registro</strong> é <strong>Ir Para</strong>, o Access se move para o registro com o número igual ao do argumento <strong>Deslocamento</strong>. O número de registros é mostrado na caixa de número de registros na parte inferior da janela.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-p107">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9f3d8-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f3d8-135">Remarks</span></span>

<span data-ttu-id="9f3d8-136">Se o foco for um controle específico em um registro, esta ação vai deixá-lo no mesmo controle do novo registro.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="9f3d8-137">Você pode usar a configuração **Novo** do argumento **Registro** para se mover para o registro em branco ao final de um formulário ou tabela para poder inserir novos dados.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="9f3d8-p108">Esta ação é semelhante a clicar na seta abaixo do botão **Localizar** da guia **Página Inicial** e clicar em **Ir Para**. Os subcomandos **Primeiro**, **Último**, **Próximo**, **Anterior** e **Novo Registro** do comando **Ir Para** têm no objeto selecionado o mesmo efeito das configurações **Primeiro**, **Último**, **Próximo**, **Anterior** e **Novo** do argumento **Registro**. Você também pode se mover para os registros usando os botões de navegação na parte inferior da janela.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-p108">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**. The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument. You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="9f3d8-141">Você poderá usar a ação **IrParaRegistro** para tornar um registro de um formulário oculto no registro atual se especificar o formulário oculto nos argumentos **Tipo de Objeto** e **Nome do Objeto**.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="9f3d8-142">Para executar a ação **IrParaRegistro** em um módulo do VBA (Visual Basic for Applications), use o método **GoToRecord** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

