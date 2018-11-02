---
title: Propriedade TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b24aaa5aec9b17adc169c67733a19a9077a4930
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920918"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="a6455-102">Propriedade TableDef.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="a6455-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="a6455-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6455-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a6455-p101">Retorna o número total de registros de um objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a6455-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6455-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6455-106">Syntax</span></span>

<span data-ttu-id="a6455-107">*expressão* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="a6455-107">*expression* .RecordCount</span></span>

<span data-ttu-id="a6455-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="a6455-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6455-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6455-109">Remarks</span></span>

<span data-ttu-id="a6455-110">Em um objeto **Recordset** ou **TableDef** sem registros, a definição da propriedade **RecordCount** é 0.</span><span class="sxs-lookup"><span data-stu-id="a6455-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="a6455-111">Quando você trabalhar com objetos vinculados**TableDef**, a definição da propriedade **RecordCount** será sempre –1.</span><span class="sxs-lookup"><span data-stu-id="a6455-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

