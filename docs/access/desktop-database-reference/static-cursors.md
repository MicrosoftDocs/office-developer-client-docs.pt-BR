---
title: Cursores estáticos (referência de banco de dados da área de trabalho do Access)
TOCTitle: Static Cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f60bce47f76214d26f75d13dece5bc062fd4db61
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889823"
---
# <a name="static-cursors"></a><span data-ttu-id="16e65-102">Cursores estáticos</span><span class="sxs-lookup"><span data-stu-id="16e65-102">Static Cursors</span></span>


<span data-ttu-id="16e65-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="16e65-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16e65-p101">O cursor estático sempre exibe o conjunto de resultados como ele era antes de o cursor ser aberto pela primeira vez. Dependendo da implementação, cursores estáticos são somente leitura ou de leitura/gravação, e fornecem rolamento de avanço e de recuo, O cursor estático geralmente não detecta alterações feitas em associações, pedidos, valores ou valores do conjunto de resultados depois que o cursor é aberto. Os cursores estáticos podem detectar suas próprias atualizações, exclusões e inserções, apesar de não serem solicitados a fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="16e65-p101">The static cursor always displays the result set as it was when the cursor was first opened. Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling. The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened. Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</span></span>

<span data-ttu-id="16e65-p102">Os cursores estátivos nunca detectam outras atualizações, exclusões e inserções. Por exemplo, suponha que um cursor estático busque uma linha e outro aplicativo, e depois atualize essa linha. Se o aplicativo buscar novamente a linha a partir do cursor estático, os valores que encontra são inalterados, apesar das alterações feitas pelo outro aplicativo. Todos os tipos de rolagem têm suporte, mas os provedores podem suportar ou não indicadores.</span><span class="sxs-lookup"><span data-stu-id="16e65-p102">Static cursors never detect other updates, deletes, and inserts. For example, suppose a static cursor fetches a row, and another application then updates that row. If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application. All types of scrolling are supported, but providers may or may not support bookmarks.</span></span>

<span data-ttu-id="16e65-p103">Se seu aplicativo não precisar detectar alterações de dados e precisar de rolagem, o cursor estático é a melhor alternativa. Use o **adOpenStatic** **CursorTypeEnum** para indicar que deseja usar um cursor estático no ADO.</span><span class="sxs-lookup"><span data-stu-id="16e65-p103">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice. Use the **adOpenStatic** **CursorTypeEnum** to indicate that you want to use a static cursor in ADO.</span></span>

