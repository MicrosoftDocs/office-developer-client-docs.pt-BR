---
title: Propriedade Recordset.Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 540e5b8226907dc580d34ab3215d3c0dca67e3f6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936879"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="c55bc-102">Propriedade Recordset.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="c55bc-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="c55bc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c55bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c55bc-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c55bc-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55bc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c55bc-106">Syntax</span></span>

<span data-ttu-id="c55bc-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="c55bc-107">*expression* .Type</span></span>

<span data-ttu-id="c55bc-108">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c55bc-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c55bc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c55bc-109">Remarks</span></span>

<span data-ttu-id="c55bc-110">Para um objeto **Recordset**, as configurações e os valores de retorno possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="c55bc-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c55bc-111">Constante</span><span class="sxs-lookup"><span data-stu-id="c55bc-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="c55bc-112">Tipo de Recordset</span><span class="sxs-lookup"><span data-stu-id="c55bc-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c55bc-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="c55bc-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="c55bc-114">Tabela (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="c55bc-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c55bc-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="c55bc-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="c55bc-116">Dinâmico (somente em espaços de trabalho ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="c55bc-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <span data-ttu-id="c55bc-p102">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c55bc-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c55bc-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="c55bc-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="c55bc-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="c55bc-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c55bc-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="c55bc-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="c55bc-122">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="c55bc-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c55bc-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="c55bc-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="c55bc-124">Somente de Encaminhamento</span><span class="sxs-lookup"><span data-stu-id="c55bc-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

