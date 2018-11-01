---
title: Enumeração QueryDefStateEnum (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b368079aeb668c9ae72e3955f55159ab2c72a53e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882564"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="694e5-102">Enumeração QueryDefStateEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="694e5-102">QueryDefStateEnum Enumeration (DAO)</span></span>


<span data-ttu-id="694e5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="694e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="694e5-104">Usada com a propriedade **Prepare** para especificar o método usado para indicar como uma consulta deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="694e5-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="694e5-105">Nome</span><span class="sxs-lookup"><span data-stu-id="694e5-105">Name</span></span></p></th>
<th><p><span data-ttu-id="694e5-106">Valor</span><span class="sxs-lookup"><span data-stu-id="694e5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="694e5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="694e5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="694e5-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="694e5-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="694e5-109">1</span><span class="sxs-lookup"><span data-stu-id="694e5-109">1</span></span></p></td>
<td><p><span data-ttu-id="694e5-110">(Padrão) A instrução é preparada (ou seja, a API de ODBC SQLPrepare é chamada).</span><span class="sxs-lookup"><span data-stu-id="694e5-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="694e5-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="694e5-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="694e5-112">2</span><span class="sxs-lookup"><span data-stu-id="694e5-112">2</span></span></p></td>
<td><p><span data-ttu-id="694e5-113">A instrução não é preparada (ou seja, a API de ODBC SQLExecDirect é chamada).</span><span class="sxs-lookup"><span data-stu-id="694e5-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

