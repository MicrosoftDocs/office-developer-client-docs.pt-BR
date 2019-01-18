---
title: Emissão de comandos para o provedor de dados subjacente
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709611"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="4a0fe-102">Emissão de comandos para o provedor de dados subjacente</span><span class="sxs-lookup"><span data-stu-id="4a0fe-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="4a0fe-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a0fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a0fe-104">Qualquer comando que não comece com SHAPE passou pelo provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="4a0fe-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="4a0fe-105">Isso equivale à emissão de um comando shape no formulário "SHAPE {provider command}".</span><span class="sxs-lookup"><span data-stu-id="4a0fe-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="4a0fe-106">Execute estes comandos *não* têm que produzir um **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4a0fe-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="4a0fe-107">Por exemplo, "SHAPE {DROP TABLE MyTable} é um comando shape perfeitamente válido, desde que o provedor de dados ofereça suporte para DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="4a0fe-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="4a0fe-108">Essa capacidade permite que ambos os comandos normais de provedor e de shape compartilhem a mesma conexão e a mesma transação.</span><span class="sxs-lookup"><span data-stu-id="4a0fe-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

