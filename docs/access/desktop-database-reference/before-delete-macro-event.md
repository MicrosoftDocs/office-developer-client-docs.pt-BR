---
title: Evento da macro Antes da Exclusão
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2b2a4f978a4af2ba79cab7807f0142d35d7d30c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296910"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="70f19-102">Evento da macro Antes da Exclusão</span><span class="sxs-lookup"><span data-stu-id="70f19-102">Before Delete macro event</span></span>

<span data-ttu-id="70f19-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70f19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70f19-104">O evento **Antes de Excluir** ocorre quando um registro é excluído, mas antes da alteração ser submetida.</span><span class="sxs-lookup"><span data-stu-id="70f19-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="70f19-105">O evento **Antes de Excluir** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="70f19-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="70f19-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="70f19-106">Remarks</span></span>

<span data-ttu-id="70f19-107">Use o evento **Antes de Excluir** para executar qualquer ação que você deseja que ocorra antes da exclusão de um registro.</span><span class="sxs-lookup"><span data-stu-id="70f19-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="70f19-108">O **Antes de Alterar** é comumente usado para executar validação e criar mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="70f19-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="70f19-109">Você pode acessar um valor no registro a ser excluído usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="70f19-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="70f19-110">Por exemplo, para acessar o valor do campo QuantityInStock no registro a ser excluído, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="70f19-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="70f19-111">Os valores contidos no registro a ser excluído são excluídos permanentemente após a conclusão do evento **Antes de Excluir**.</span><span class="sxs-lookup"><span data-stu-id="70f19-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="70f19-112">Você pode cancelar o evento **Antes de Excluir** utilizando a ação **GerarErro**.</span><span class="sxs-lookup"><span data-stu-id="70f19-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="70f19-113">Quando um erro é gerado, as alterações contidas no evento **Antes de Excluir** são descartadas.</span><span class="sxs-lookup"><span data-stu-id="70f19-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="70f19-114">A tabela a seguir lista comandos de macro que podem ser usadas no evento **Antes de Excluir**.</span><span class="sxs-lookup"><span data-stu-id="70f19-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70f19-115">Tipo de Comando</span><span class="sxs-lookup"><span data-stu-id="70f19-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="70f19-116">Comando</span><span class="sxs-lookup"><span data-stu-id="70f19-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70f19-117">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="70f19-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="70f19-118"><a href="comment-macro-statement.md">Instrução de macro Comentário</a></span><span class="sxs-lookup"><span data-stu-id="70f19-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70f19-119">Fluxo do Programa</span><span class="sxs-lookup"><span data-stu-id="70f19-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="70f19-120"><a href="group-macro-statement.md">Instrução de macro Grupo</a></span><span class="sxs-lookup"><span data-stu-id="70f19-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70f19-121">Fluxo do Programa</span><span class="sxs-lookup"><span data-stu-id="70f19-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="70f19-122"><a href="if-then-else-macro-block.md">Bloco de macro Se... Então... Senão</a></span><span class="sxs-lookup"><span data-stu-id="70f19-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70f19-123">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="70f19-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="70f19-124"><a href="lookuprecord-data-block.md">Ação da macro LookupRecord</a></span><span class="sxs-lookup"><span data-stu-id="70f19-124"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70f19-125">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="70f19-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="70f19-126"><a href="clearmacroerror-macro-action.md">Ação de macro LimparErrodaMacro</a></span><span class="sxs-lookup"><span data-stu-id="70f19-126"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70f19-127">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="70f19-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="70f19-128"><a href="onerror-macro-action.md">Ação de macro AoOcorrerErro</a></span><span class="sxs-lookup"><span data-stu-id="70f19-128"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70f19-129">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="70f19-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="70f19-130"><a href="raiseerror-macro-action.md">Ação de macro GerarErro</a></span><span class="sxs-lookup"><span data-stu-id="70f19-130"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70f19-131">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="70f19-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="70f19-132"><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></span><span class="sxs-lookup"><span data-stu-id="70f19-132"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70f19-133">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="70f19-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="70f19-134"><a href="stopmacro-macro-action.md">Ação de macro PararMacro</a></span><span class="sxs-lookup"><span data-stu-id="70f19-134"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70f19-135">Para criar uma Macro de Dados que capture o evento **Antes de Excluir**, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="70f19-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="70f19-136">Abra a tabela na qual deseja capturar o evento **Antes de Excluir**.</span><span class="sxs-lookup"><span data-stu-id="70f19-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="70f19-137">Na guia **Tabela,** no grupo Antes de **Eventos,** selecione **Antes de Excluir.**</span><span class="sxs-lookup"><span data-stu-id="70f19-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

