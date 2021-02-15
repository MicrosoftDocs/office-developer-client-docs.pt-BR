---
title: Bloco de dados EditarRegiscord
TOCTitle: EditRecord data block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32ddfbbf21e62d5967fa1f2f31bab0222664eb39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293592"
---
# <a name="editrecord-data-block"></a><span data-ttu-id="0ea16-102">Bloco de dados EditarRegiscord</span><span class="sxs-lookup"><span data-stu-id="0ea16-102">EditRecord data block</span></span>

<span data-ttu-id="0ea16-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ea16-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ea16-104">Você pode usar o bloco de dados **EditarRegistro** para alterar os valores contidos em um registro existente.</span><span class="sxs-lookup"><span data-stu-id="0ea16-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span>

> [!NOTE]
> <span data-ttu-id="0ea16-105">O bloco de dados **EditarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="0ea16-105">The **EditRecord** data block is available only in Data Macros.</span></span>


## <a name="setting"></a><span data-ttu-id="0ea16-106">Setting</span><span class="sxs-lookup"><span data-stu-id="0ea16-106">Setting</span></span>

<span data-ttu-id="0ea16-107">O bloco de dados **EditarRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="0ea16-107">The **EditRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ea16-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="0ea16-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="0ea16-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ea16-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ea16-110"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="0ea16-110"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea16-111">Uma cadeia de caracteres que identifica o registro a ser editado.</span><span class="sxs-lookup"><span data-stu-id="0ea16-111">A string that identifies the record to edit.</span></span> <span data-ttu-id="0ea16-112">Se o argumento <em>Alias</em> não for especificado, o registro atual será editado.</span><span class="sxs-lookup"><span data-stu-id="0ea16-112">If the <em>Alias</em> argument is not specified, then the current record is edited.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="0ea16-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ea16-113">Remarks</span></span>

<span data-ttu-id="0ea16-p102">Após a instrução **EditarRegistro**, você pode inserir um bloco de comandos que será executado antes da atribuição das alterações do registro. As ações a seguir estão disponíveis em bloco de dados **EditarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="0ea16-p102">After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted. The following actions are available in a **EditRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ea16-116"><a href="cancelrecordchange-macro-action.md">Ação de macro CancelarAlteraçãodeRegistro</a></span><span class="sxs-lookup"><span data-stu-id="0ea16-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea16-117"><a href="comment-macro-statement.md">Instrução de macro Comentário</a></span><span class="sxs-lookup"><span data-stu-id="0ea16-117"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea16-118"><a href="group-macro-statement.md">Instrução de macro Grupo</a></span><span class="sxs-lookup"><span data-stu-id="0ea16-118"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea16-119"><a href="if-then-else-macro-block.md">Se... Então... Instrução de macro Else</a></span><span class="sxs-lookup"><span data-stu-id="0ea16-119"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea16-120"><a href="setfield-macro-action.md">Ação de macro DefinirCampo</a></span><span class="sxs-lookup"><span data-stu-id="0ea16-120"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea16-121"><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></span><span class="sxs-lookup"><span data-stu-id="0ea16-121"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0ea16-122">Use a ação **DefinirCampo** para especificar os novos valores de um campo no registro editado.</span><span class="sxs-lookup"><span data-stu-id="0ea16-122">Use the **SetField** action to specify the new values of a field in the edited record.</span></span>

<span data-ttu-id="0ea16-123">Você pode usar uma instrução **Se...Então...Senão** para executar operações com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="0ea16-123">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="0ea16-p103">Para cancelar a edição de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **EditarRegistro** é encerrado.</span><span class="sxs-lookup"><span data-stu-id="0ea16-p103">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span>

<span data-ttu-id="0ea16-126">Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="0ea16-126">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="0ea16-127">Por exemplo, use a sintaxe a seguir para se referir ao campo AtribuídoA do registro criado mais recentemente:</span><span class="sxs-lookup"><span data-stu-id="0ea16-127">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="0ea16-128">O bloco de dados CriarRegistro somente pode ser usado nos eventos de macro de dados **[Após Inserir](after-insert-macro-event.md)**, **[Após Atualizar](after-update-macro-event.md)** e **[Após Atualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="0ea16-128">The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

