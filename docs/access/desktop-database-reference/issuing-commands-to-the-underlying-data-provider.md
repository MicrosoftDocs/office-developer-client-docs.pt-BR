---
title: Emitindo comandos para o provedor de dados subjacente
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 142772aaff5080a6e2522ab31884f2ff2319c8a7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944631"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="b89d4-102">Emitindo comandos para o provedor de dados subjacente</span><span class="sxs-lookup"><span data-stu-id="b89d4-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="b89d4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b89d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b89d4-104">Qualquer comando que não comece com SHAPE passou pelo provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="b89d4-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="b89d4-105">Isso equivale à emissão de um comando shape no formulário "SHAPE {provider command}".</span><span class="sxs-lookup"><span data-stu-id="b89d4-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="b89d4-106">Execute estes comandos *não* têm que produzir um **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b89d4-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="b89d4-107">Por exemplo, "SHAPE {DROP TABLE MyTable} é um comando shape perfeitamente válido, desde que o provedor de dados ofereça suporte para DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="b89d4-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="b89d4-108">Essa capacidade permite que ambos os comandos normais de provedor e de shape compartilhem a mesma conexão e a mesma transação.</span><span class="sxs-lookup"><span data-stu-id="b89d4-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

