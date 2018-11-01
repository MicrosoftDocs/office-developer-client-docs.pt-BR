---
title: Método Recordset.MoveNext (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef9d90e16ea4c98add8557cdeae22cb85caeeb64
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884314"
---
# <a name="recordsetmovenext-method-dao"></a><span data-ttu-id="a8ebf-102">Método Recordset.MoveNext (DAO)</span><span class="sxs-lookup"><span data-stu-id="a8ebf-102">Recordset.MoveNext Method (DAO)</span></span>


<span data-ttu-id="a8ebf-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8ebf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8ebf-104">Move o próximo registro em um objeto **Recordset** especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-104">Moves to the next record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ebf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8ebf-105">Syntax</span></span>

<span data-ttu-id="a8ebf-106">*expressão* . MoveNext</span><span class="sxs-lookup"><span data-stu-id="a8ebf-106">*expression* .MoveNext</span></span>

<span data-ttu-id="a8ebf-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a8ebf-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ebf-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8ebf-108">Remarks</span></span>

<span data-ttu-id="a8ebf-109">Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="a8ebf-p101">Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="a8ebf-p102">Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="a8ebf-p103">Se você usar o **MoveNext** quando o último registro for o atual, a propriedade **EOF** será **True**, e não haverá nenhum registro atual. Se você usar **MoveNext** novamente, ocorrerá um erro, e **EOF** permanece **True**.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-p103">If you use **MoveNext** when the last record is current, the **EOF** property is **True**, and there is no current record. If you use **MoveNext** again, an error occurs, and **EOF** remains **True**.</span></span>

<span data-ttu-id="a8ebf-116">Se o recordset se refere a um tipo tabela **Recordset** (somente espaços de trabalho do Microsoft Access), o movimento segue o índice atual.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="a8ebf-117">Você pode definir o índice atual utilizando a propriedade **Index**.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="a8ebf-118">Se você não definir o índice atual, a ordem dos registros retornados será indefinida.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="a8ebf-119">Você não pode usar os métodos **MoveFirst**, **MoveLast**e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="a8ebf-120">Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.</span><span class="sxs-lookup"><span data-stu-id="a8ebf-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

