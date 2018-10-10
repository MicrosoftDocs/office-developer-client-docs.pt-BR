---
title: Método Recordset2.MovePrevious (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d437fe3bb271cc50c187b185bcd3078b523a73a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462184"
---
# <a name="recordset2moveprevious-method-dao"></a><span data-ttu-id="199fb-102">Método Recordset2.MovePrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="199fb-102">Recordset2.MovePrevious Method (DAO)</span></span>


<span data-ttu-id="199fb-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="199fb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="199fb-104">Move o registro anterior em um objeto **Recordset** especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="199fb-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="199fb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="199fb-105">Syntax</span></span>

<span data-ttu-id="199fb-106">*expressão* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="199fb-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="199fb-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="199fb-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="199fb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="199fb-108">Remarks</span></span>

<span data-ttu-id="199fb-109">Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.</span><span class="sxs-lookup"><span data-stu-id="199fb-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="199fb-p101">Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="199fb-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="199fb-p102">Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.</span><span class="sxs-lookup"><span data-stu-id="199fb-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="199fb-p103">Se você usar o **MovePrevious** quando o primeiro registro for o atual, a propriedade **BOF** será **True**, e não haverá nenhum registro atual. Se você usar **MovePrevious** novamente, ocorrerá um erro, e **BOF** permanece **True**.</span><span class="sxs-lookup"><span data-stu-id="199fb-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="199fb-116">Se o recordset se refere a um tipo tabela **Recordset** (somente espaços de trabalho do Microsoft Access), o movimento segue o índice atual.</span><span class="sxs-lookup"><span data-stu-id="199fb-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="199fb-117">Você pode definir o índice atual utilizando a propriedade **Index**.</span><span class="sxs-lookup"><span data-stu-id="199fb-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="199fb-118">Se você não definir o índice atual, a ordem dos registros retornados será indefinida.</span><span class="sxs-lookup"><span data-stu-id="199fb-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="199fb-119">Você não pode usar os métodos **MoveFirst**, **MoveLast**e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="199fb-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="199fb-120">Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.</span><span class="sxs-lookup"><span data-stu-id="199fb-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

