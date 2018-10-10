---
title: Cursores dinâmicos (referência de banco de dados da área de trabalho do Access)
TOCTitle: Dynamic Cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c324923f0e702ad59ac120ea5de2eebcccd260e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461954"
---
# <a name="dynamic-cursors"></a><span data-ttu-id="01a74-102">Cursores dinâmicos</span><span class="sxs-lookup"><span data-stu-id="01a74-102">Dynamic Cursors</span></span>


<span data-ttu-id="01a74-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="01a74-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="01a74-p101">Os cursores dinâmicos detectam todas as alterações feitas nas linhas do conjunto de resultados, independentemente de as alterações ocorrerem dentro do cursor ou por outros usuários fora dele. Todas as instruções de inserção, atualização e exclusão realizadas por todos os usuários podem ser vistas através do cursor. O cursor dinâmico pode detectar as alterações feitas nas linhas, na ordem e nos valores do conjunto de resultados após a abertura do cursor. As atualizações feitas fora do cursor não ficam visíveis até que sejam confirmadas (a não ser que o nível de isolamento de transações do cursor seja definido como "não confirmado").</span><span class="sxs-lookup"><span data-stu-id="01a74-p101">Dynamic cursors detect all changes made to the rows in the result set, regardless of whether the changes occur from inside the cursor or by other users outside the cursor. All insert, update, and delete statements made by all users are visible through the cursor. The dynamic cursor can detect any changes made to the rows, order, and values in the result set after the cursor is opened. Updates made outside the cursor are not visible until they are committed (unless the cursor transaction isolation level is set to "uncommitted").</span></span>

<span data-ttu-id="01a74-p102">Por exemplo, suponha que um cursor dinâmico busque duas linhas e outro aplicativo e, em seguida, atualize uma dessas linha e exclua a outra. Se o cursor dinâmico buscar essas linhas, ele não encontrará a linha excluída, mas exibirá os novos valores referentes à linha atualizada.</span><span class="sxs-lookup"><span data-stu-id="01a74-p102">For example, suppose a dynamic cursor fetches two rows and another application, and then updates one of those rows and deletes the other. If the dynamic cursor then fetches those rows, it will not find the deleted row, but it will display the new values for the updated row.</span></span>

<span data-ttu-id="01a74-p103">O cursor dinâmico será uma boa opção se seu aplicativo precisar detectar todas as atualizações simultâneas realizadas por outros usuários. Use **adOpenDynamic** **CursorTypeEnum** para indicar que você deseja usar um cursor dinâmico no ADO.</span><span class="sxs-lookup"><span data-stu-id="01a74-p103">The dynamic cursor is a good choice if your application must detect all concurrent updates made by other users. Use the **adOpenDynamic** **CursorTypeEnum** to indicate that you want to use a dynamic cursor in ADO.</span></span>

<span data-ttu-id="01a74-112">[Cursores apenas de avanço](forward-only-cursors.md) | [Cursores estáticos](static-cursors.md) | [Cursores de conjunto de chaves](keyset-cursors.md)</span><span class="sxs-lookup"><span data-stu-id="01a74-112">[Forward-Only Cursors](forward-only-cursors.md) | [Static Cursors](static-cursors.md) | [Keyset Cursors](keyset-cursors.md)</span></span>

