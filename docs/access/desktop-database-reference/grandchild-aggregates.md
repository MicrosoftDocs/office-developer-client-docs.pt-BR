---
title: Agregações de netos
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722155"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="585e7-102">Agregações de netos</span><span class="sxs-lookup"><span data-stu-id="585e7-102">Grandchild aggregates</span></span>


<span data-ttu-id="585e7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="585e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="585e7-104">A coluna de capítulo criada em uma cláusula de um comando de forma pode ser dado um *nome de alias de capítulo* (geralmente com a palavra-chave).</span><span class="sxs-lookup"><span data-stu-id="585e7-104">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword).</span></span> <span data-ttu-id="585e7-105">Você pode identificar qualquer coluna qualquer capítulo do **Recordset** com formato com um nome totalmente qualificado que identifica o filho que contém a coluna.</span><span class="sxs-lookup"><span data-stu-id="585e7-105">You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column.</span></span> <span data-ttu-id="585e7-106">Por exemplo, se o capítulo pai, Cap1, contém um capítulo de filho, chap2, que tem uma coluna de quantidade amt, então o nome qualificado seria chap1.chap2.amt. O nome qualificado, em seguida, pode ser usado como um argumento para uma das funções agregadas (soma, média, MAX, MIN, contagem, DESVPAD ou qualquer).</span><span class="sxs-lookup"><span data-stu-id="585e7-106">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>

