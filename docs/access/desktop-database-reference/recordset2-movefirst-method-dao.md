---
title: Método Recordset2.MoveFirst (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 74b186d0-8f6a-d136-a563-04f58d67b122
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195879(v=office.15)
ms:contentKeyID: 48545667
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a54658e1259a49a1c92facf988076e6b6e1dd961
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309657"
---
# <a name="recordset2movefirst-method-dao"></a><span data-ttu-id="21982-102">Método Recordset2.MoveFirst (DAO)</span><span class="sxs-lookup"><span data-stu-id="21982-102">Recordset2.MoveFirst method (DAO)</span></span>


<span data-ttu-id="21982-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21982-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21982-104">Move para o primeiro registro em um objeto **Recordset** específico e o torna o registro atual. </span><span class="sxs-lookup"><span data-stu-id="21982-104">Moves to the first record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="21982-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21982-105">Syntax</span></span>

<span data-ttu-id="21982-106">*expressão* .MoveFirst</span><span class="sxs-lookup"><span data-stu-id="21982-106">*expression* .MoveFirst</span></span>

<span data-ttu-id="21982-107">*expressão* Uma variável que representa **um objeto Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="21982-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21982-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="21982-108">Remarks</span></span>

<span data-ttu-id="21982-109">Use os métodos **Move** para mover de um registro para outro sem aplicar nenhuma condição.</span><span class="sxs-lookup"><span data-stu-id="21982-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="21982-p101">Se você editar o registro atual, certifique-se de usar o método **Update** para salvar as alterações antes de mover para outro registro. Se você mover para outro registro sem realizar a atualização, as alterações serão perdidas sem nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="21982-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="21982-p102">Quando você abre um **Recordset**, o primeiro registro é o atual, e a propriedade **BOF** é **False**. Se o **Recordset** não contiver nenhum registro, a propriedade **BOF** será **True**, e não haverá nenhum registro atual.</span><span class="sxs-lookup"><span data-stu-id="21982-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="21982-114">Se o primeiro ou o último registro já for o atual quando você usar **MoveFirst** ou **MoveLast**, o registro atual não será alterado.</span><span class="sxs-lookup"><span data-stu-id="21982-114">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="21982-115">Se o recordset se referir a um tipo de tabela **Recordset**(apenas espaços de trabalho do Microsoft Access), a movimentação seguirá o índice atual.</span><span class="sxs-lookup"><span data-stu-id="21982-115">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="21982-116">Você pode definir o índice atual utilizando a propriedade **Index**.</span><span class="sxs-lookup"><span data-stu-id="21982-116">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="21982-117">Se você não definir o índice atual, a ordem dos registros retornados será indefinida.</span><span class="sxs-lookup"><span data-stu-id="21982-117">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="21982-118">Você não pode usar os métodos **MoveFirst**, **MoveLast** e **MovePrevious** em um objeto **Recordset** do tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="21982-118">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="21982-119">Para mover a posição do registro atual em um número específico de registros do objeto **Recordset** para frente ou para trás, use o método **Move**.</span><span class="sxs-lookup"><span data-stu-id="21982-119">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

