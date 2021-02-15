---
title: Propriedade ActiveCommand (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281926"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="164d3-102">Propriedade ActiveCommand (ADO)</span><span class="sxs-lookup"><span data-stu-id="164d3-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="164d3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="164d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="164d3-104">Indica o objeto [Command](command-object-ado.md) que criou o objeto [Recordset](recordset-object-ado.md) associado.</span><span class="sxs-lookup"><span data-stu-id="164d3-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="164d3-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="164d3-105">Return value</span></span>

<span data-ttu-id="164d3-106">Retorna um **Variant** contendo um objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="164d3-106">Returns a **Variant** that contains a **Command** object.</span></span> <span data-ttu-id="164d3-107">O padrão é uma referência nula ao objeto.</span><span class="sxs-lookup"><span data-stu-id="164d3-107">Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="164d3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="164d3-108">Remarks</span></span>

<span data-ttu-id="164d3-109">A propriedade **ActiveCommand** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="164d3-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="164d3-110">Se um **objeto Command** não tiver sido usado para criar o **Recordset atual,** uma referência de objeto **Null** será retornada.</span><span class="sxs-lookup"><span data-stu-id="164d3-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="164d3-111">Use essa propriedade para encontrar o objeto **Command** associado quando receber apenas o objeto **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="164d3-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

