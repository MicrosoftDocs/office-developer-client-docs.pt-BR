---
title: Enumeração QueryDefStateEnum (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68f6f1e96ae57508d94ea341b36e3a6b32cac660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464033"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="7c7c4-102">Enumeração QueryDefStateEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c7c4-102">QueryDefStateEnum Enumeration (DAO)</span></span>


<span data-ttu-id="7c7c4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c7c4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7c7c4-104">Usada com a propriedade **Prepare** para especificar o método usado para indicar como uma consulta deve ser preparada.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c7c4-105">Nome</span><span class="sxs-lookup"><span data-stu-id="7c7c4-105">Name</span></span></p></th>
<th><p><span data-ttu-id="7c7c4-106">Valor</span><span class="sxs-lookup"><span data-stu-id="7c7c4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7c7c4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c7c4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c7c4-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="7c7c4-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="7c7c4-109">1</span><span class="sxs-lookup"><span data-stu-id="7c7c4-109">1</span></span></p></td>
<td><p><span data-ttu-id="7c7c4-110">(Padrão) A instrução é preparada (ou seja, a API de ODBC SQLPrepare é chamada).</span><span class="sxs-lookup"><span data-stu-id="7c7c4-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7c4-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="7c7c4-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="7c7c4-112">2</span><span class="sxs-lookup"><span data-stu-id="7c7c4-112">2</span></span></p></td>
<td><p><span data-ttu-id="7c7c4-113">A instrução não é preparada (ou seja, a API de ODBC SQLExecDirect é chamada).</span><span class="sxs-lookup"><span data-stu-id="7c7c4-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

