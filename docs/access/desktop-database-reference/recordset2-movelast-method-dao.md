---
title: Método Recordset2. moVelast (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 829c4dd759bce86388cc65aa5b63276eec438ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307256"
---
# <a name="recordset2movelast-method-dao"></a><span data-ttu-id="06bfd-102">Método Recordset2. moVelast (DAO)</span><span class="sxs-lookup"><span data-stu-id="06bfd-102">Recordset2.MoveLast method (DAO)</span></span>

<span data-ttu-id="06bfd-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06bfd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06bfd-104">Move o último registro em um objeto **Recordset** especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="06bfd-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="06bfd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06bfd-105">Syntax</span></span>

<span data-ttu-id="06bfd-106">*expressão* . MoVelast (***Opções***)</span><span class="sxs-lookup"><span data-stu-id="06bfd-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="06bfd-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="06bfd-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="06bfd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06bfd-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06bfd-109">Nome</span><span class="sxs-lookup"><span data-stu-id="06bfd-109">Name</span></span></p></th>
<th><p><span data-ttu-id="06bfd-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="06bfd-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="06bfd-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="06bfd-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="06bfd-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="06bfd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06bfd-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="06bfd-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="06bfd-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="06bfd-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="06bfd-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="06bfd-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="06bfd-116">Defina para <strong>dbRunAsync</strong> para executar a chamada de <strong>MoveLast</strong> de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="06bfd-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="06bfd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="06bfd-117">Remarks</span></span>

<span data-ttu-id="06bfd-118">Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.</span><span class="sxs-lookup"><span data-stu-id="06bfd-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="06bfd-p101">Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="06bfd-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="06bfd-p102">Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.</span><span class="sxs-lookup"><span data-stu-id="06bfd-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="06bfd-123">Se o primeiro ou o último registro já for o atual quando você usar **MoveFirst** ou **MoveLast**, o registro atual não será alterado.</span><span class="sxs-lookup"><span data-stu-id="06bfd-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="06bfd-124">Se Recordset se refere a um **Recordset** do tipo tabela (somente espaços de trabalho do Microsoft Access), o movimento segue o índice atual.</span><span class="sxs-lookup"><span data-stu-id="06bfd-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="06bfd-125">Você pode definir o índice atual utilizando a propriedade **Index**.</span><span class="sxs-lookup"><span data-stu-id="06bfd-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="06bfd-126">Se você não definir o índice atual, a ordem dos registros retornados será indefinida.</span><span class="sxs-lookup"><span data-stu-id="06bfd-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="06bfd-127">[!OBSERVAçãO] Você pode usar o método **MoveLast** para preencher totalmente um **Recordset** do tipo dynaset ou instantâneo para fornecer o número atual de registros no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="06bfd-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="06bfd-128">Contudo, se você utilizar **MoveLast** dessa forma, poderá reduzir o desempenho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06bfd-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="06bfd-129">Utilize **MoveLast** somente se for absolutamente necessário para obter uma conta de registro precisa em um **Recordset** recém aberto.</span><span class="sxs-lookup"><span data-stu-id="06bfd-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
>
> <span data-ttu-id="06bfd-130">Se você usa a constante **dbRunAsync** com **MoveLast**, a chamada do método é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="06bfd-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="06bfd-131">É possível usar a propriedade **StillExecuting** para determinar quando o **Recordset** é totalmente preenchido, e o método **Cancel** para determinar a execução da chamada assíncrona do método **MoveLast**.</span><span class="sxs-lookup"><span data-stu-id="06bfd-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="06bfd-132">Você não pode usar os métodos **MoveFirst**, MoveLast e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="06bfd-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="06bfd-133">Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.</span><span class="sxs-lookup"><span data-stu-id="06bfd-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

