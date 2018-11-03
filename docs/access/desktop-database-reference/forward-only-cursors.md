---
title: Cursores somente de encaminhamento
TOCTitle: Forward-only cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e742e3a6903faf7ab817b79675b100d026e25885
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946759"
---
# <a name="forward-only-cursors"></a><span data-ttu-id="50319-102">Cursores somente de encaminhamento</span><span class="sxs-lookup"><span data-stu-id="50319-102">Forward-only cursors</span></span>

<span data-ttu-id="50319-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="50319-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50319-p101">O tipo de cursor padrão comum, chamado cursor apenas de avanço (ou não-rolável), pode mover apenas para frente no conjunto de resultados. Um cursor apenas de avanço não oferece suporte para rolagem (a capacidade de mover para frente e para trás no conjunto de resultados); ele só oferece suporte à busca de linhas do início ao fim desse conjunto. Com alguns cursores apenas de avanço (como os da biblioteca de cursores do SQL Server), todas instruções de inserção, atualização e exclusão realizadas pelo usuário final (ou confirmadas por outros usuários) que afetam linhas no conjunto de resultados ficam visíveis à medida que as linhas são buscadas. No entanto, como o cursor não pode ser rolado para trás, as alterações feitas nas linhas do banco de dados após a busca da linha não ficam visíveis através do cursor.</span><span class="sxs-lookup"><span data-stu-id="50319-p101">The typical default cursor type, called a forward-only (or non-scrollable) cursor, can move only forward through the result set. A forward-only cursor does not support scrolling (the ability to move forward and backward in the result set); it only supports fetching rows from the start to the end of the result set. With some forward-only cursors (such as with the SQL Server cursor library), all insert, update, and delete statements made by the current user (or committed by other users) that affect rows in the result set are visible as the rows are fetched. Because the cursor cannot be scrolled backward, however, changes made to rows in the database after the row was fetched are not visible through the cursor.</span></span>

<span data-ttu-id="50319-p102">Depois que os dados da linha atual são processados, o cursor apenas de avanço libera os recursos que foram usados para armazenar os dados. Os cursores apenas de avanço são dinâmicos por padrão, significando que todas as alterações são detectadas à medida que a linha atual é processada. Consequentemente, a abertura do cursor torna-se mais rápida, permitindo que o conjunto de resultados exiba as atualizações feitas nas tabelas subjacentes.</span><span class="sxs-lookup"><span data-stu-id="50319-p102">After the data for the current row is processed, the forward-only cursor releases the resources that were used to hold that data. Forward-only cursors are dynamic by default, meaning that all changes are detected as the current row is processed. This provides faster cursor opening and enables the result set to display updates made to the underlying tables.</span></span>

<span data-ttu-id="50319-p103">Como os cursores apenas de avanço não oferecem suporte à rolagem para trás, seu aplicativo pode retornar ao início do conjunto de resultados fechando e reabrindo o cursor. Essa é uma maneira eficiente de trabalhar com pequenos volumes de dados. Como alternativa, o aplicativo pode ler o conjunto de resultados uma vez, armazenar os dados no cache local e, depois, navegar nesse cache.</span><span class="sxs-lookup"><span data-stu-id="50319-p103">While forward-only cursors do not support backward scrolling, your application can return to the beginning of the result set by closing and reopening the cursor. This is an effective way to work with small amounts of data. As an alternative, your application could read the result set once, cache the data locally, and then browse the local data cache.</span></span>

<span data-ttu-id="50319-p104">Se o seu aplicativo não exigir rolagem no conjunto de resultados, o cursor apenas de avanço será a melhor maneira de recuperar dados rapidamente com sobrecarga mínima. Use **adOpenForwardOnly** **CursorTypeEnum** para indicar que você deseja usar um cursor apenas de avanço no ADO.</span><span class="sxs-lookup"><span data-stu-id="50319-p104">If your application does not require scrolling through the result set, the forward-only cursor is the best way to retrieve data quickly with the least amount of overhead. Use the **adOpenForwardOnly** **CursorTypeEnum** to indicate that you want to use a forward-only cursor in ADO.</span></span>

