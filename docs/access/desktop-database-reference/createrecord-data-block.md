---
title: Bloco de dados CriarRegistro
TOCTitle: CreateRecord Data Block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bda30265cbcf2377114734d03b16f889b0d165b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880814"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="4c4ba-102">Bloco de dados CriarRegistro</span><span class="sxs-lookup"><span data-stu-id="4c4ba-102">CreateRecord Data Block</span></span>


<span data-ttu-id="4c4ba-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c4ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c4ba-104">Você pode usar o bloco de dados **CriarRegistro** para criar um novo registro na tabela especificada.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="4c4ba-105">[!OBSERVAçãO] O bloco de dados **CriarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="4c4ba-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="4c4ba-106">Setting</span></span>

<span data-ttu-id="4c4ba-107">O bloco de dados **ExcluirRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c4ba-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="4c4ba-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="4c4ba-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4c4ba-109">Required</span></span></p></th>
<th><p><span data-ttu-id="4c4ba-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c4ba-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c4ba-111"><strong>Criar Registro em</strong></span><span class="sxs-lookup"><span data-stu-id="4c4ba-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="4c4ba-112">Sim</span><span class="sxs-lookup"><span data-stu-id="4c4ba-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="4c4ba-113">O nome da tabela onde o novo registro será criado.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c4ba-114"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="4c4ba-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="4c4ba-115">Não</span><span class="sxs-lookup"><span data-stu-id="4c4ba-115">No</span></span></p></td>
<td><p><span data-ttu-id="4c4ba-116">Uma cadeia de caracteres que identifica o registro.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-116">An string that identifies the record.</span></span> <span data-ttu-id="4c4ba-117">Você pode usar o alias do registro para identificá-lo</span><span class="sxs-lookup"><span data-stu-id="4c4ba-117">You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4c4ba-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c4ba-118">Remarks</span></span>

<span data-ttu-id="4c4ba-119">O registro criado por **CriarRegistro** se torna automaticamente o registro atual.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="4c4ba-120">Após a instrução **CriarRegistro** , você pode inserir um bloco de comandos que executará antes o novo registro é submetido.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-120">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="4c4ba-121">As ações a seguir estão disponíveis em bloco de dados **CriarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-121">The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c4ba-122"><a href="cancelrecordchange-macro-action.md">Ação de macro CancelRecordChange</a></span><span class="sxs-lookup"><span data-stu-id="4c4ba-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c4ba-123"><a href="comment-macro-statement.md">Instrução de macro de comentário</a></span><span class="sxs-lookup"><span data-stu-id="4c4ba-123"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c4ba-124"><a href="group-macro-statement.md">Instrução de macro de grupo</a></span><span class="sxs-lookup"><span data-stu-id="4c4ba-124"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c4ba-125"><a href="if-then-else-macro-block.md">Se... Então... Instrução de Macro Else</a></span><span class="sxs-lookup"><span data-stu-id="4c4ba-125"><a href="if-then-else-macro-block.md">If...Then...Else Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c4ba-126"><a href="setfield-macro-action.md">Ação de macro SetField</a></span><span class="sxs-lookup"><span data-stu-id="4c4ba-126"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c4ba-127"><a href="setlocalvar-macro-action.md">Ação de macro SetLocalVar</a></span><span class="sxs-lookup"><span data-stu-id="4c4ba-127"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4c4ba-128">Depois que a ação **CriarRegistro** criar um registro, use a ação **DefinirCampo** para especificar o valor de um campo no novo registro.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="4c4ba-129">Você pode usar uma instrução **Se...Então...Senão** para executar operações com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="4c4ba-p103">Para cancelar a criação de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **CriarRegistro** é encerrado.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-p103">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="4c4ba-132">Quando o novo registro for atribuído, você poderá usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o registro.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-132">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="4c4ba-133">Por exemplo, use a sintaxe a seguir para se referir ao campo AssignedTo do registro mais recentemente criado.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-133">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="4c4ba-134">O bloco de dados **CriarRegistro** somente pode ser usado nos eventos de macro de dados **[Após Inserir](after-insert-macro-event.md)**, **[Após Atualizar](after-update-macro-event.md)** e **[Após Atualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="4c4ba-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

