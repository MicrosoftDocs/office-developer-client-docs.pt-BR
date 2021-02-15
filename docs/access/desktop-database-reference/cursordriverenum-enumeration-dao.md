---
title: Enumeração cursorDriverEnum (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f2bf52943a84d6f2e60891d63810bc0bbb6ecb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295244"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="b4979-102">Enumeração cursorDriverEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="b4979-102">CursorDriverEnum enumeration (DAO)</span></span>

<span data-ttu-id="b4979-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4979-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4979-104">Especifica o tipo de driver de cursor.</span><span class="sxs-lookup"><span data-stu-id="b4979-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4979-105">Nome</span><span class="sxs-lookup"><span data-stu-id="b4979-105">Name</span></span></p></th>
<th><p><span data-ttu-id="b4979-106">Valor</span><span class="sxs-lookup"><span data-stu-id="b4979-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b4979-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4979-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4979-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="b4979-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="b4979-109">3 </span><span class="sxs-lookup"><span data-stu-id="b4979-109">3</span></span></p></td>
<td><p><span data-ttu-id="b4979-p101">Sempre utiliza a Biblioteca de Cursores do FoxPro. Esta opção é necessária para executar atualizações em lotes.</span><span class="sxs-lookup"><span data-stu-id="b4979-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4979-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="b4979-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="b4979-113">-1</span><span class="sxs-lookup"><span data-stu-id="b4979-113">-1</span></span></p></td>
<td><p><span data-ttu-id="b4979-114">(Padrão) Utiliza cursores do servidor se este oferecer suporte; caso contrário, usa a Biblioteca de Cursores ODBC.</span><span class="sxs-lookup"><span data-stu-id="b4979-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4979-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="b4979-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="b4979-116">4 </span><span class="sxs-lookup"><span data-stu-id="b4979-116">4</span></span></p></td>
<td><p><span data-ttu-id="b4979-117">Abre todos os cursores (isto é, objetos <strong>Recordset</strong>) como tipo somente de encaminhamento, somente leitura, com tamanho 1 de conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="b4979-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="b4979-118">Também conhecidas como &quot; consultas sem cursor.&quot;</span><span class="sxs-lookup"><span data-stu-id="b4979-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4979-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="b4979-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="b4979-120">1 </span><span class="sxs-lookup"><span data-stu-id="b4979-120">1</span></span></p></td>
<td><p><span data-ttu-id="b4979-p103">Sempre utiliza a Biblioteca de Cursores ODBC. Esta opção fornece melhor desempenho para pequenos conjuntos de resultados, mas se degrada rapidamente em conjuntos de resultados maiores.</span><span class="sxs-lookup"><span data-stu-id="b4979-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4979-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="b4979-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="b4979-124">2 </span><span class="sxs-lookup"><span data-stu-id="b4979-124">2</span></span></p></td>
<td><p><span data-ttu-id="b4979-p104">Sempre utiliza cursores do servidor. Para a maioria das grandes operações esta opção oferece melhor desempenho, mas pode gerar mais tráfego na rede.</span><span class="sxs-lookup"><span data-stu-id="b4979-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

