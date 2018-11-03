---
title: Enumeração CursorDriverEnum (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8fac1dbf3da20e3af476ec4bcaac6046d834881
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944099"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="824c4-102">Enumeração CursorDriverEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="824c4-102">CursorDriverEnum enumeration (DAO)</span></span>

<span data-ttu-id="824c4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="824c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="824c4-104">Especifica o tipo de driver de cursor.</span><span class="sxs-lookup"><span data-stu-id="824c4-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="824c4-105">Nome</span><span class="sxs-lookup"><span data-stu-id="824c4-105">Name</span></span></p></th>
<th><p><span data-ttu-id="824c4-106">Valor</span><span class="sxs-lookup"><span data-stu-id="824c4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="824c4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="824c4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="824c4-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="824c4-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="824c4-109">3</span><span class="sxs-lookup"><span data-stu-id="824c4-109">3</span></span></p></td>
<td><p><span data-ttu-id="824c4-p101">Sempre utiliza a Biblioteca de Cursores do FoxPro. Esta opção é necessária para executar atualizações em lotes.</span><span class="sxs-lookup"><span data-stu-id="824c4-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="824c4-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="824c4-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="824c4-113">-1</span><span class="sxs-lookup"><span data-stu-id="824c4-113">-1</span></span></p></td>
<td><p><span data-ttu-id="824c4-114">(Padrão) Utiliza cursores do servidor se este oferecer suporte; caso contrário, usa a Biblioteca de Cursores ODBC.</span><span class="sxs-lookup"><span data-stu-id="824c4-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="824c4-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="824c4-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="824c4-116">4</span><span class="sxs-lookup"><span data-stu-id="824c4-116">4</span></span></p></td>
<td><p><span data-ttu-id="824c4-117">Abre todos os cursores (ou seja, objetos <strong>Recordset</strong> ) como tipo somente de encaminhamento, como somente leitura, com um tamanho de conjunto de linhas de 1.</span><span class="sxs-lookup"><span data-stu-id="824c4-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="824c4-118">Também conhecido como &quot;consultas sem cursor.&quot;</span><span class="sxs-lookup"><span data-stu-id="824c4-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="824c4-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="824c4-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="824c4-120">1</span><span class="sxs-lookup"><span data-stu-id="824c4-120">1</span></span></p></td>
<td><p><span data-ttu-id="824c4-p103">Sempre utiliza a Biblioteca de Cursores ODBC. Esta opção fornece melhor desempenho para pequenos conjuntos de resultados, mas se degrada rapidamente em conjuntos de resultados maiores.</span><span class="sxs-lookup"><span data-stu-id="824c4-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="824c4-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="824c4-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="824c4-124">2</span><span class="sxs-lookup"><span data-stu-id="824c4-124">2</span></span></p></td>
<td><p><span data-ttu-id="824c4-p104">Sempre utiliza cursores do servidor. Para a maioria das grandes operações esta opção oferece melhor desempenho, mas pode gerar mais tráfego na rede.</span><span class="sxs-lookup"><span data-stu-id="824c4-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

