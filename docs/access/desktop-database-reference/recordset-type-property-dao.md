---
title: Propriedade Recordset.Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85e518dc5d13a6e8e70c449fb35158395b7a13aa
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920722"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="f86c5-102">Propriedade Recordset.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="f86c5-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="f86c5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f86c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f86c5-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f86c5-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86c5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f86c5-106">Syntax</span></span>

<span data-ttu-id="f86c5-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="f86c5-107">*expression* .Type</span></span>

<span data-ttu-id="f86c5-108">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f86c5-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f86c5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f86c5-109">Remarks</span></span>

<span data-ttu-id="f86c5-110">Para um objeto **Recordset**, as configurações e os valores de retorno possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f86c5-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f86c5-111">Constante</span><span class="sxs-lookup"><span data-stu-id="f86c5-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="f86c5-112">Tipo de Recordset</span><span class="sxs-lookup"><span data-stu-id="f86c5-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f86c5-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="f86c5-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="f86c5-114">Tabela (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="f86c5-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f86c5-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="f86c5-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="f86c5-116">Dinâmico (somente em espaços de trabalho ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="f86c5-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="f86c5-p102">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f86c5-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f86c5-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="f86c5-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="f86c5-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="f86c5-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f86c5-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="f86c5-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="f86c5-122">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="f86c5-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f86c5-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="f86c5-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="f86c5-124">Somente de Encaminhamento</span><span class="sxs-lookup"><span data-stu-id="f86c5-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

