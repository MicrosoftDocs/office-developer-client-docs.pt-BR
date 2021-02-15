---
title: Significado do local do cursor
TOCTitle: The Significance of Cursor Location
ms:assetid: 57cf91a0-2612-b1ca-1c03-9c1ccb396b2e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249296(v=office.15)
ms:contentKeyID: 48544978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3ae9cc65d61416767140572b32d3f2e1b8e4d8eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313976"
---
# <a name="significance-of-cursor-location"></a><span data-ttu-id="4e1d1-102">Significado de local do cursor</span><span class="sxs-lookup"><span data-stu-id="4e1d1-102">Significance of cursor location</span></span>

<span data-ttu-id="4e1d1-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e1d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e1d1-p101">Todo cursor usa recursos temporários para manter seus dados. Esses recursos podem ser a memória, um arquivo de paginação de disco, arquivos de disco temporários ou mesmo repositório temporário no banco de dados. O cursor é chamado cursor *do lado do cliente* quando esses recursos estão localizados no computador do cliente. E é chamado cursor *do servidor* quando esses recursos estão localizados no servidor.</span><span class="sxs-lookup"><span data-stu-id="4e1d1-p101">Every cursor uses temporary resources to hold its data. These resources can be memory, a disk paging file, temporary disk files, or even temporary storage in the database. The cursor is called a *client-side* cursor when these resources are located on the client computer. The cursor is called a *server-side* cursor when these resources are located on the server.</span></span>

## <a name="client-side-cursors"></a><span data-ttu-id="4e1d1-108">Cursores do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="4e1d1-108">Client-Side Cursors</span></span>

<span data-ttu-id="4e1d1-p102">No ADO, chame um cursor do lado do cliente usando **adUseClient** **CursorLocationEnum**. Com um cursor do lado do cliente que não seja de conjunto de chaves, o servidor envia o conjunto de resultados inteiro para o computador cliente, através da rede. O computador cliente fornece e gerencia os recursos temporários necessários para o cursor e o conjunto de resultados. O aplicativo do lado do cliente pode navegar no conjunto de resultados inteiro para determinar quais são as linhas necessárias.</span><span class="sxs-lookup"><span data-stu-id="4e1d1-p102">In ADO, call for a client-side cursor by using the **adUseClient** **CursorLocationEnum**. With a non-keyset client-side cursor, the server sends the entire result set across the network to the client computer. The client computer provides and manages the temporary resources needed by the cursor and result set. The client-side application can browse through the entire result set to determine which rows it requires.</span></span>

<span data-ttu-id="4e1d1-p103">Os cursores do lado do cliente, estáticos e controlados por conjuntos de chaves, podem representar uma carga significativa para a estação de trabalho, caso incluam linhas em excesso. Embora todas as bibliotecas de cursores sejam capazes de criar cursores com milhares de linhas, os aplicativos desenvolvidos para buscar esses grandes conjuntos de linhas podem apresentar um desempenho insatisfatório. Há exceções, é claro. Para alguns aplicativos, um cursor grande do lado do cliente pode ser perfeitamente adequado e o desempenho pode não ser um problema.</span><span class="sxs-lookup"><span data-stu-id="4e1d1-p103">Static and keyset-driven client-side cursors may place a significant load on your workstation if they include too many rows. While all of the cursor libraries are capable of building cursors with thousands of rows, applications designed to fetch such large rowsets may perform poorly. There are exceptions, of course. For some applications, a large client-side cursor might be perfectly appropriate and performance might not be an issue.</span></span>

<span data-ttu-id="4e1d1-p104">Um benefício óbvio do cursor do lado do cliente é a resposta rápida. Após o conjunto de resultados ser baixado no computador cliente, a navegação pelas linhas é muito rápida. O aplicativo em geral é mais escalonável com os cursores do lado do cliente, pois as necessidades de recursos do cursor são colocadas separadamente em cada cliente, e não no servidor.</span><span class="sxs-lookup"><span data-stu-id="4e1d1-p104">One obvious benefit of the client-side cursor is quick response. After the result set has been downloaded to the client computer, browsing through the rows is very fast. Your application is generally more scalable with client-side cursors because the cursor's resource requirements are placed on each separate client and not on the server.</span></span>

## <a name="server-side-cursors"></a><span data-ttu-id="4e1d1-120">Cursores do servidor</span><span class="sxs-lookup"><span data-stu-id="4e1d1-120">Server-Side Cursors</span></span>

<span data-ttu-id="4e1d1-p105">No ADO, chame um cursor do servidor usando **adUseServer** **CursorLocationEnum**. Com esse cursor, o servidor gerencia o conjunto de resultados usando recursos fornecidos pelo computador servidor. O cursor do servidor retorna através da rede apenas os dados solicitados. Esse tipo de cursor às vezes pode oferecer um desempenho melhor do que o cursor do lado do cliente, especialmente em situações nas quais o tráfego excessivo da rede é um problema.</span><span class="sxs-lookup"><span data-stu-id="4e1d1-p105">In ADO, call for a server-side cursor by using the **adUseServer** **CursorLocationEnum.** With a server-side cursor, the server manages the result set using resources provided by the server computer. The server-side cursor returns only the requested data over the network. This type of cursor can sometimes provide better performance than the client-side cursor, especially in situations where excessive network traffic is a problem.</span></span>

<span data-ttu-id="4e1d1-p106">No entanto, é importante observar que um cursor do servidor está  pelo menos temporariamente  consumindo recursos preciosos do servidor para cada cliente ativo. É necessário planejamento para garantir que o hardware do servidor consiga gerenciar todos os cursores do servidor solicitados pelos clientes ativos. Além disso, esse cursor pode ser lento, pois fornece apenas acesso a linha única  não há cursor em lote disponível.</span><span class="sxs-lookup"><span data-stu-id="4e1d1-p106">However, it is important to point out that a server-side cursor is — at least temporarily — consuming precious server resources for every active client. You must plan accordingly to ensure that your server hardware is capable of managing all of the server-side cursors requested by active clients. Also, a server-side cursor can be slow because it provides only single row access — there is no batch cursor available.</span></span>

<span data-ttu-id="4e1d1-p107">Os cursores do servidor são úteis para inclusão, atualização ou exclusão de registros. Com eles, é possível ter várias instruções ativas na mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="4e1d1-p107">Server-side cursors are useful when inserting, updating, or deleting records. With server-side cursors, you can have multiple active statements on the same connection.</span></span>

