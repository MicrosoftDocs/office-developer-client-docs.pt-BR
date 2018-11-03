---
title: 'Capítulo 8: Noções básicas sobre cursores e bloqueios'
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ca76b5635e057251aff845ecf45146e6e0d89a6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936935"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="c06be-102">Capítulo 8: Noções básicas sobre cursores e bloqueios</span><span class="sxs-lookup"><span data-stu-id="c06be-102">Chapter 8: Understanding cursors and locks</span></span>

<span data-ttu-id="c06be-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c06be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c06be-p101">É importante saber como os cursores operam, para poder selecionar o melhor e mais eficiente tipo de cursor para as necessidades de acesso aos dados do aplicativo. Uma configuração do cursor abaixo da ideal pode tornar as operações de acesso aos dados terrivelmente lentas.</span><span class="sxs-lookup"><span data-stu-id="c06be-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="c06be-106">Muitos recursos do objeto **Recordset** do ADO são determinados pelo tipo e local do cursor, bem como pelo tipo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c06be-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="c06be-107">Este capítulo aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="c06be-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="c06be-108">O que é um cursor?</span><span class="sxs-lookup"><span data-stu-id="c06be-108">What is a cursor?</span></span>](what-is-a-cursor.md)
- [<span data-ttu-id="c06be-109">Significado do local do cursor</span><span class="sxs-lookup"><span data-stu-id="c06be-109">The significance of cursor location</span></span>](the-significance-of-cursor-location.md)
- [<span data-ttu-id="c06be-110">Microsoft Cursor Service for OLE DB</span><span class="sxs-lookup"><span data-stu-id="c06be-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)
- [<span data-ttu-id="c06be-111">Usando CacheSize</span><span class="sxs-lookup"><span data-stu-id="c06be-111">Using CacheSize</span></span>](using-cachesize.md)
- [<span data-ttu-id="c06be-112">Características de bloqueio e cursor</span><span class="sxs-lookup"><span data-stu-id="c06be-112">Cursor and lock characteristics</span></span>](cursor-and-lock-characteristics.md)
- [<span data-ttu-id="c06be-113">Tipos de cursores (ADO)</span><span class="sxs-lookup"><span data-stu-id="c06be-113">Types of cursors (ADO)</span></span>](types-of-cursors.md)
- [<span data-ttu-id="c06be-114">O que é um bloqueio? (ADO)</span><span class="sxs-lookup"><span data-stu-id="c06be-114">What is a lock? (ADO)</span></span>](what-is-a-lock.md)

