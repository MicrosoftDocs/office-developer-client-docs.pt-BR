---
title: Enumeração DeryDefStateEnum (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303315"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="ee78f-102">Enumeração DeryDefStateEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="ee78f-102">QueryDefStateEnum enumeration (DAO)</span></span>


<span data-ttu-id="ee78f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee78f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee78f-104">Usada com a propriedade **Prepare** para especificar o método usado para indicar como uma consulta deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="ee78f-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee78f-105">Nome</span><span class="sxs-lookup"><span data-stu-id="ee78f-105">Name</span></span></p></th>
<th><p><span data-ttu-id="ee78f-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ee78f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ee78f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee78f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee78f-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="ee78f-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="ee78f-109">1 </span><span class="sxs-lookup"><span data-stu-id="ee78f-109">1</span></span></p></td>
<td><p><span data-ttu-id="ee78f-110">(Padrão) A instrução é preparada (ou seja, a API de ODBC SQLPrepare é chamada).</span><span class="sxs-lookup"><span data-stu-id="ee78f-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee78f-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="ee78f-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="ee78f-112">2 </span><span class="sxs-lookup"><span data-stu-id="ee78f-112">2</span></span></p></td>
<td><p><span data-ttu-id="ee78f-113">A instrução não é preparada (ou seja, a API de ODBC SQLExecDirect é chamada).</span><span class="sxs-lookup"><span data-stu-id="ee78f-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

