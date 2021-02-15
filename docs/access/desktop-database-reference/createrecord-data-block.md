---
title: Bloco de dados CriarRegiscord
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295349"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="e936a-102">Bloco de dados CriarRegiscord</span><span class="sxs-lookup"><span data-stu-id="e936a-102">CreateRecord data block</span></span>


<span data-ttu-id="e936a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e936a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e936a-104">Você pode usar o bloco de dados **CriarRegistro** para criar um novo registro na tabela especificada.</span><span class="sxs-lookup"><span data-stu-id="e936a-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="e936a-105">O bloco de dados **CriarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="e936a-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="e936a-106">Setting</span><span class="sxs-lookup"><span data-stu-id="e936a-106">Setting</span></span>

<span data-ttu-id="e936a-107">O bloco de dados **ExcluirRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e936a-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e936a-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="e936a-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="e936a-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e936a-109">Required</span></span></p></th>
<th><p><span data-ttu-id="e936a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e936a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e936a-111"><strong>Criar Registro em</strong></span><span class="sxs-lookup"><span data-stu-id="e936a-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="e936a-112">Sim</span><span class="sxs-lookup"><span data-stu-id="e936a-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="e936a-113">O nome da tabela onde o novo registro será criado.</span><span class="sxs-lookup"><span data-stu-id="e936a-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e936a-114"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="e936a-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="e936a-115">Não</span><span class="sxs-lookup"><span data-stu-id="e936a-115">No</span></span></p></td>
<td><p><span data-ttu-id="e936a-116">Uma cadeia de caracteres que identifica o registro.</span><span class="sxs-lookup"><span data-stu-id="e936a-116">An string that identifies the record.</span></span> <span data-ttu-id="e936a-117">Você pode usar o alias do registro para identificá-lo</span><span class="sxs-lookup"><span data-stu-id="e936a-117">You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e936a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e936a-118">Remarks</span></span>

<span data-ttu-id="e936a-119">O registro criado por **CriarRegistro** se torna automaticamente o registro atual.</span><span class="sxs-lookup"><span data-stu-id="e936a-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="e936a-120">Após **a instrução CreateRecord,** você pode inserir um bloco de comandos que será executado antes da confirmação do novo registro.</span><span class="sxs-lookup"><span data-stu-id="e936a-120">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="e936a-121">As ações a seguir estão disponíveis em bloco de dados **CriarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="e936a-121">The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e936a-122"><a href="cancelrecordchange-macro-action.md">Ação de macro CancelarAlteraçãodeRegistro</a></span><span class="sxs-lookup"><span data-stu-id="e936a-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e936a-123"><a href="comment-macro-statement.md">Instrução de macro Comentário</a></span><span class="sxs-lookup"><span data-stu-id="e936a-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e936a-124"><a href="group-macro-statement.md">Instrução de macro Grupo</a></span><span class="sxs-lookup"><span data-stu-id="e936a-124"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e936a-125"><a href="if-then-else-macro-block.md">Se... Então... Instrução de macro Else</a></span><span class="sxs-lookup"><span data-stu-id="e936a-125"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e936a-126"><a href="setfield-macro-action.md">Ação de macro DefinirCampo</a></span><span class="sxs-lookup"><span data-stu-id="e936a-126"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e936a-127"><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></span><span class="sxs-lookup"><span data-stu-id="e936a-127"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e936a-128">Depois que a ação **CriarRegistro** criar um registro, use a ação **DefinirCampo** para especificar o valor de um campo no novo registro.</span><span class="sxs-lookup"><span data-stu-id="e936a-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="e936a-129">Você pode usar uma instrução **Se...Então...Senão** para executar operações com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="e936a-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="e936a-p103">Para cancelar a criação de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **CriarRegistro** é encerrado.</span><span class="sxs-lookup"><span data-stu-id="e936a-p103">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="e936a-132">Quando o novo registro for atribuído, você poderá usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o registro.</span><span class="sxs-lookup"><span data-stu-id="e936a-132">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="e936a-133">Por exemplo, use a sintaxe a seguir para referir-se ao campo AtribuídoA do registro criado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="e936a-133">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="e936a-134">O bloco de dados **CriarRegistro** somente pode ser usado nos eventos de macro de dados **[Após Inserir](after-insert-macro-event.md)**, **[Após Atualizar](after-update-macro-event.md)** e **[Após Atualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="e936a-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

