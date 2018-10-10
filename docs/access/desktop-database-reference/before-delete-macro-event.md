---
title: Evento de macro Antes de Excluir
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7863f8500a81014f3c70b5547fb363c46803f4f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464214"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="2b1b1-102">Evento de macro Antes de Excluir</span><span class="sxs-lookup"><span data-stu-id="2b1b1-102">Before Delete Macro Event</span></span>

<span data-ttu-id="2b1b1-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b1b1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2b1b1-104">O evento **Antes de Excluir** ocorre quando um registro é excluído, mas antes da alteração ser submetida.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="2b1b1-105">[!OBSERVAçãO] O evento **Antes de Excluir** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b1b1-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b1b1-106">Remarks</span></span>

<span data-ttu-id="2b1b1-107">Use o evento **Antes de Excluir** para executar qualquer ação que você deseja que ocorra antes da exclusão de um registro.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="2b1b1-108">O **Antes de Alterar** é comumente usado para executar validação e criar mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="2b1b1-109">Você pode acessar um valor no registro a ser excluído utilizando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="2b1b1-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="2b1b1-110">Por exemplo, para acessar o valor do campo Quantidadeemestoque no registro a ser excluído, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="2b1b1-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="2b1b1-111">Os valores contidos no registro a ser excluído são excluídos permanentemente após a conclusão do evento **Antes de Excluir**.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="2b1b1-112">Você pode cancelar o evento **Antes de Excluir** utilizando a ação **GerarErro**.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="2b1b1-113">Quando um erro é gerado, as alterações contidas no evento **Antes de excluir** são descartadas.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="2b1b1-114">A tabela a seguir lista comandos de macro que podem ser usadas no evento **Antes de Excluir**.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b1b1-115">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="2b1b1-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="2b1b1-116">Comando</span><span class="sxs-lookup"><span data-stu-id="2b1b1-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b1b1-117">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="2b1b1-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2b1b1-118"><a href="comment-macro-statement.md">Instrução de macro de comentário</a></span><span class="sxs-lookup"><span data-stu-id="2b1b1-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b1b1-119">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="2b1b1-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2b1b1-120"><a href="group-macro-statement.md">Instrução de macro de grupo</a></span><span class="sxs-lookup"><span data-stu-id="2b1b1-120"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b1b1-121">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="2b1b1-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2b1b1-122"><a href="if-then-else-macro-block.md">Bloco de macro If...Then...Else</a></span><span class="sxs-lookup"><span data-stu-id="2b1b1-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b1b1-123">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="2b1b1-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2b1b1-124"><a href="lookuprecord-data-block.md">Ação de Macro Pesquisarregistro</a></span><span class="sxs-lookup"><span data-stu-id="2b1b1-124"><a href="lookuprecord-data-block.md">LookupRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b1b1-125">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2b1b1-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2b1b1-126"><a href="clearmacroerror-macro-action.md">Ação de macro ClearMacroError</a></span><span class="sxs-lookup"><span data-stu-id="2b1b1-126"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b1b1-127">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2b1b1-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2b1b1-128"><a href="onerror-macro-action.md">Ação de macro OnError</a></span><span class="sxs-lookup"><span data-stu-id="2b1b1-128"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b1b1-129">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2b1b1-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2b1b1-130"><a href="raiseerror-macro-action.md">Ação de macro RaiseError</a></span><span class="sxs-lookup"><span data-stu-id="2b1b1-130"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b1b1-131">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2b1b1-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2b1b1-132"><a href="setlocalvar-macro-action.md">Ação de macro SetLocalVar</a></span><span class="sxs-lookup"><span data-stu-id="2b1b1-132"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b1b1-133">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2b1b1-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2b1b1-134"><a href="stopmacro-macro-action.md">Ação de macro StopMacro</a></span><span class="sxs-lookup"><span data-stu-id="2b1b1-134"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2b1b1-135">Para criar uma Macro de Dados que capture o evento **Antes de Excluir**, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="2b1b1-136">Abra a tabela na qual deseja capturar o evento **Antes de Excluir**.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="2b1b1-137">Na guia **tabela** , no grupo **Antes de eventos** , selecione **Antes de excluir**.</span><span class="sxs-lookup"><span data-stu-id="2b1b1-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

