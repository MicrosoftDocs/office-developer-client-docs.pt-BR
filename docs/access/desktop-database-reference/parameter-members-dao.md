---
title: Membros parameter (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288109"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="55ff7-102">Membros parameter (DAO)</span><span class="sxs-lookup"><span data-stu-id="55ff7-102">Parameter members (DAO)</span></span>

<span data-ttu-id="55ff7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55ff7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55ff7-104">Um objeto Parameter representa um valor fornecido para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="55ff7-104">A Parameter object represents a value supplied to a query.</span></span> <span data-ttu-id="55ff7-105">O parâmetro está associado ao objeto QueryDef criado a partir de uma consulta parâmetro.</span><span class="sxs-lookup"><span data-stu-id="55ff7-105">The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="55ff7-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55ff7-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55ff7-107">Nome</span><span class="sxs-lookup"><span data-stu-id="55ff7-107">Name</span></span></p></th>
<th><p><span data-ttu-id="55ff7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="55ff7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55ff7-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span><span class="sxs-lookup"><span data-stu-id="55ff7-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55ff7-110"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="55ff7-110"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="55ff7-111">Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="55ff7-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="55ff7-112">Define ou retorna um valor que indica se um objeto <strong><a href="parameter-object-dao.md">Parameter</a></strong> representa um parâmetro de entrada, um parâmetro de saída, ambos ou o valor de retorno do procedimento (apenas espaços de trabalho do ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="55ff7-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55ff7-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="55ff7-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55ff7-114">Retorna o nome do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="55ff7-114">Returns the name of the specified object.</span></span> <span data-ttu-id="55ff7-115"><strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="55ff7-115">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55ff7-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="55ff7-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55ff7-117">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="55ff7-117">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="55ff7-118">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="55ff7-118">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55ff7-119"><strong><a href="parameter-type-property-dao.md">Tipo</a></strong></span><span class="sxs-lookup"><span data-stu-id="55ff7-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55ff7-120">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto.</span><span class="sxs-lookup"><span data-stu-id="55ff7-120">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="55ff7-121"><strong>número inteiro</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="55ff7-121">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55ff7-122"><strong><a href="parameter-value-property-dao.md">Valor</a></strong></span><span class="sxs-lookup"><span data-stu-id="55ff7-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55ff7-123">Define ou retorna o valor de um objeto.</span><span class="sxs-lookup"><span data-stu-id="55ff7-123">Sets or returns the value of an object.</span></span> <span data-ttu-id="55ff7-124"><strong>Variant</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="55ff7-124">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

