---
title: Propriedade TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1d1ab4fee16a9664733c71522cb07a49dde149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463757"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="ffdc4-102">Propriedade TableDef.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="ffdc4-102">TableDef.RecordCount Property (DAO)</span></span>


<span data-ttu-id="ffdc4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffdc4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ffdc4-p101">Retorna o número total de registros de um objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffdc4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffdc4-106">Syntax</span></span>

<span data-ttu-id="ffdc4-107">*expressão* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="ffdc4-107">*expression* .RecordCount</span></span>

<span data-ttu-id="ffdc4-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="ffdc4-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffdc4-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffdc4-109">Remarks</span></span>

<span data-ttu-id="ffdc4-110">Em um objeto **Recordset** ou **TableDef** sem registros, a definição da propriedade **RecordCount** é 0.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="ffdc4-111">Quando você trabalhar com objetos vinculados**TableDef**, a definição da propriedade **RecordCount** será sempre –1.</span><span class="sxs-lookup"><span data-stu-id="ffdc4-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

