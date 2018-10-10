---
title: Método Recordset.MoveLast (DAO)
TOCTitle: MoveLast Method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c154a576a4ac1aedf555ba8164bc243fe49a3841
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464165"
---
# <a name="recordsetmovelast-method-dao"></a><span data-ttu-id="d2224-102">Método Recordset.MoveLast (DAO)</span><span class="sxs-lookup"><span data-stu-id="d2224-102">Recordset.MoveLast Method (DAO)</span></span>


<span data-ttu-id="d2224-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2224-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d2224-104">Move o último registro em um objeto **Recordset** especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="d2224-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2224-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2224-105">Syntax</span></span>

<span data-ttu-id="d2224-106">*expressão* . MoveLast (***Opções***)</span><span class="sxs-lookup"><span data-stu-id="d2224-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="d2224-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d2224-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="d2224-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2224-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2224-109">Nome</span><span class="sxs-lookup"><span data-stu-id="d2224-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d2224-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="d2224-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="d2224-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d2224-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="d2224-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2224-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2224-113">Opções</span><span class="sxs-lookup"><span data-stu-id="d2224-113">Options</span></span></p></td>
<td><p><span data-ttu-id="d2224-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="d2224-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d2224-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="d2224-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="d2224-116">Defina para <strong>dbRunAsync</strong> para executar a chamada de <strong>MoveLast</strong> de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d2224-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d2224-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2224-117">Remarks</span></span>

<span data-ttu-id="d2224-118">Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.</span><span class="sxs-lookup"><span data-stu-id="d2224-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="d2224-p101">Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="d2224-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="d2224-p102">Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.</span><span class="sxs-lookup"><span data-stu-id="d2224-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="d2224-123">Se o primeiro ou o último registro já for o atual quando você usar **MoveFirst** ou **MoveLast**, o registro atual não será alterado.</span><span class="sxs-lookup"><span data-stu-id="d2224-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="d2224-124">Se o recordset se refere a um tipo tabela **Recordset** (somente espaços de trabalho do Microsoft Access), o movimento segue o índice atual.</span><span class="sxs-lookup"><span data-stu-id="d2224-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="d2224-125">Você pode definir o índice atual utilizando a propriedade **Index**.</span><span class="sxs-lookup"><span data-stu-id="d2224-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="d2224-126">Se você não definir o índice atual, a ordem dos registros retornados será indefinida.</span><span class="sxs-lookup"><span data-stu-id="d2224-126">If you don't set the current index, the order of returned records is undefined.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d2224-p104">[!OBSERVAçãO] Você pode usar o método <STRONG>MoveLast</STRONG> para preencher totalmente um <STRONG>Recordset</STRONG> do tipo dynaset ou instantâneo para fornecer o número atual de registros no <STRONG>Recordset</STRONG>. Contudo, se você utilizar <STRONG>MoveLast</STRONG> dessa forma, poderá reduzir o desempenho do aplicativo. Utilize <STRONG>MoveLast</STRONG> somente se for absolutamente necessário para obter uma conta de registro precisa em um <STRONG>Recordset</STRONG> recém aberto. Se você usa a constante <STRONG>dbRunAsync</STRONG> com <STRONG>MoveLast</STRONG>, a chamada do método é assíncrona. É possível usar a propriedade <STRONG>StillExecuting</STRONG> para determinar quando o <STRONG>Recordset</STRONG> é totalmente preenchido, e o método <STRONG>Cancel</STRONG> para determinar a execução da chamada assíncrona do método <STRONG>MoveLast</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d2224-p104">You can use the <STRONG>MoveLast</STRONG> method to fully populate a dynaset- or snapshot-type <STRONG>Recordset</STRONG> to provide the current number of records in the <STRONG>Recordset</STRONG>. However, if you use <STRONG>MoveLast</STRONG> in this way, you can slow down your application's performance. You should only use <STRONG>MoveLast</STRONG> to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened <STRONG>Recordset</STRONG>. If you use the <STRONG>dbRunAsync</STRONG> constant with <STRONG>MoveLast</STRONG>, the method call is asynchronous. You can use the <STRONG>StillExecuting</STRONG> property to determine when the <STRONG>Recordset</STRONG> is fully populated, and you can use the <STRONG>Cancel</STRONG> method to terminate execution of the asynchronous <STRONG>MoveLast</STRONG> method call.</span></span></P>



<span data-ttu-id="d2224-132">Você não pode usar os métodos **MoveFirst**, **MoveLast**e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="d2224-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="d2224-133">Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.</span><span class="sxs-lookup"><span data-stu-id="d2224-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

