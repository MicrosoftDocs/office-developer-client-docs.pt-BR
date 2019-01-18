---
title: Método Recordset2.MoveNext (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0eeb917e-f76a-03ec-9e1e-aa8d501db031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845265(v=office.15)
ms:contentKeyID: 48543254
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6f500578182aac74b608117ee4105a6b657057df
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719908"
---
# <a name="recordset2movenext-method-dao"></a><span data-ttu-id="a8616-102">Método Recordset2.MoveNext (DAO)</span><span class="sxs-lookup"><span data-stu-id="a8616-102">Recordset2.MoveNext method (DAO)</span></span>


<span data-ttu-id="a8616-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8616-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8616-104">Move o próximo registro em um objeto **Recordset** especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="a8616-104">Moves to the next record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8616-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8616-105">Syntax</span></span>

<span data-ttu-id="a8616-106">*expressão* . MoveNext</span><span class="sxs-lookup"><span data-stu-id="a8616-106">*expression* .MoveNext</span></span>

<span data-ttu-id="a8616-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="a8616-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8616-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8616-108">Remarks</span></span>

<span data-ttu-id="a8616-109">Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.</span><span class="sxs-lookup"><span data-stu-id="a8616-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="a8616-p101">Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="a8616-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="a8616-p102">Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.</span><span class="sxs-lookup"><span data-stu-id="a8616-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="a8616-p103">Se você usar o **MoveNext** quando o último registro for o atual, a propriedade **EOF** será **True**, e não haverá nenhum registro atual. Se você usar **MoveNext** novamente, ocorrerá um erro, e **EOF** permanece **True**.</span><span class="sxs-lookup"><span data-stu-id="a8616-p103">If you use **MoveNext** when the last record is current, the **EOF** property is **True**, and there is no current record. If you use **MoveNext** again, an error occurs, and **EOF** remains **True**.</span></span>

<span data-ttu-id="a8616-116">Se o recordset se refere a um tipo tabela **Recordset** (somente espaços de trabalho do Microsoft Access), o movimento segue o índice atual.</span><span class="sxs-lookup"><span data-stu-id="a8616-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="a8616-117">Você pode definir o índice atual utilizando a propriedade **Index**.</span><span class="sxs-lookup"><span data-stu-id="a8616-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="a8616-118">Se você não definir o índice atual, a ordem dos registros retornados será indefinida.</span><span class="sxs-lookup"><span data-stu-id="a8616-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="a8616-119">Você não pode usar os métodos **MoveFirst**, **MoveLast**e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="a8616-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="a8616-120">Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.</span><span class="sxs-lookup"><span data-stu-id="a8616-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

