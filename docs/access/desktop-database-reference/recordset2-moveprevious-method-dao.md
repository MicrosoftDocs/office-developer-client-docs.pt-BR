---
title: Método Recordset2.MovePrevious (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9753d3bbb586e2c1bd44755deb529758d8eab060
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307242"
---
# <a name="recordset2moveprevious-method-dao"></a><span data-ttu-id="1a101-102">Método Recordset2.MovePrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="1a101-102">Recordset2.MovePrevious method (DAO)</span></span>


<span data-ttu-id="1a101-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a101-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a101-104">Move para o registro anterior em um objeto **Recordset** específico e o torna o registro atual. </span><span class="sxs-lookup"><span data-stu-id="1a101-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a101-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a101-105">Syntax</span></span>

<span data-ttu-id="1a101-106">*expressão* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="1a101-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="1a101-107">*expressão* Uma variável que representa **um objeto Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="1a101-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a101-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a101-108">Remarks</span></span>

<span data-ttu-id="1a101-109">Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.</span><span class="sxs-lookup"><span data-stu-id="1a101-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="1a101-p101">Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="1a101-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="1a101-p102">Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.</span><span class="sxs-lookup"><span data-stu-id="1a101-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="1a101-p103">Se você usar o **MovePrevious** quando o primeiro registro for o atual, a propriedade **BOF** será **True**, e não haverá nenhum registro atual. Se você usar **MovePrevious** novamente, ocorrerá um erro, e **BOF** permanece **True**.</span><span class="sxs-lookup"><span data-stu-id="1a101-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="1a101-116">Se o recordset se referir a um tipo de tabela **Recordset**(apenas espaços de trabalho do Microsoft Access), a movimentação seguirá o índice atual.</span><span class="sxs-lookup"><span data-stu-id="1a101-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="1a101-117">Você pode definir o índice atual utilizando a propriedade **Index**.</span><span class="sxs-lookup"><span data-stu-id="1a101-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="1a101-118">Se você não definir o índice atual, a ordem dos registros retornados será indefinida.</span><span class="sxs-lookup"><span data-stu-id="1a101-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="1a101-119">Você não pode usar os métodos **MoveFirst**, **MoveLast** e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="1a101-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="1a101-120">Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.</span><span class="sxs-lookup"><span data-stu-id="1a101-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

