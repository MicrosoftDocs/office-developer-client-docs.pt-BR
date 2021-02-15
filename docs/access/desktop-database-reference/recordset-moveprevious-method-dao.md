---
title: Método Recordset.MovePrevious (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 82a3bc3e-5221-9a1a-1350-47bc6759edeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196699(v=office.15)
ms:contentKeyID: 48545984
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052872
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 95cf5daa9eac6644b17f47b09ebc749bd9ed928e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284508"
---
# <a name="recordsetmoveprevious-method-dao"></a><span data-ttu-id="7b74b-102">Método Recordset.MovePrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="7b74b-102">Recordset.MovePrevious method (DAO)</span></span>


<span data-ttu-id="7b74b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b74b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b74b-104">Move para o registro anterior em um objeto **Recordset** específico e o torna o registro atual. </span><span class="sxs-lookup"><span data-stu-id="7b74b-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b74b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b74b-105">Syntax</span></span>

<span data-ttu-id="7b74b-106">*expressão* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="7b74b-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="7b74b-107">*expression* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7b74b-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b74b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b74b-108">Remarks</span></span>

<span data-ttu-id="7b74b-109">Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.</span><span class="sxs-lookup"><span data-stu-id="7b74b-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="7b74b-p101">Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="7b74b-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="7b74b-p102">Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.</span><span class="sxs-lookup"><span data-stu-id="7b74b-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="7b74b-p103">Se você usar o **MovePrevious** quando o primeiro registro for o atual, a propriedade **BOF** será **True**, e não haverá nenhum registro atual. Se você usar **MovePrevious** novamente, ocorrerá um erro, e **BOF** permanece **True**.</span><span class="sxs-lookup"><span data-stu-id="7b74b-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="7b74b-116">Se o recordset se referir a um tipo de tabela **Recordset**(apenas espaços de trabalho do Microsoft Access), a movimentação seguirá o índice atual.</span><span class="sxs-lookup"><span data-stu-id="7b74b-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="7b74b-117">Você pode definir o índice atual utilizando a propriedade **Index**.</span><span class="sxs-lookup"><span data-stu-id="7b74b-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="7b74b-118">Se você não definir o índice atual, a ordem dos registros retornados será indefinida.</span><span class="sxs-lookup"><span data-stu-id="7b74b-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="7b74b-119">Você não pode usar os métodos **MoveFirst**, **MoveLast** e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="7b74b-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="7b74b-120">Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.</span><span class="sxs-lookup"><span data-stu-id="7b74b-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

