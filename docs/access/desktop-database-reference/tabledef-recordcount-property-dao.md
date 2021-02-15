---
title: Propriedade TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314284"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="3163a-102">Propriedade TableDef.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="3163a-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="3163a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3163a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3163a-104">Retorna o número total de registros de um objeto **[TableDef](tabledef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="3163a-104">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="3163a-105">**Long** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3163a-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3163a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3163a-106">Syntax</span></span>

<span data-ttu-id="3163a-107">*expressão* .RecordCount</span><span class="sxs-lookup"><span data-stu-id="3163a-107">*expression* .RecordCount</span></span>

<span data-ttu-id="3163a-108">*expressão* Uma variável que representa um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="3163a-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3163a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3163a-109">Remarks</span></span>

<span data-ttu-id="3163a-110">Um objeto **Recordset** ou **TableDef** sem registros tem a propriedade **RecordCount** configurada como 0.</span><span class="sxs-lookup"><span data-stu-id="3163a-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="3163a-111">Quando você trabalhar com objetos vinculados **TableDef**, a definição da propriedade **RecordCount** será sempre –1.</span><span class="sxs-lookup"><span data-stu-id="3163a-111">When you work with linked **TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

