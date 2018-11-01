---
title: Emitindo comandos para o provedor de dados adjacente
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0379d38b6c38145a72d5ab41b7ee0e7ec45531b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889074"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="36d88-102">Emitindo comandos para o provedor de dados adjacente</span><span class="sxs-lookup"><span data-stu-id="36d88-102">Issuing Commands to the Underlying Data Provider</span></span>


<span data-ttu-id="36d88-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="36d88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36d88-104">Qualquer comando que não comece com SHAPE passou pelo provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="36d88-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="36d88-105">Isso equivale à emissão de um comando shape no formulário "SHAPE {provider command}".</span><span class="sxs-lookup"><span data-stu-id="36d88-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="36d88-106">Execute estes comandos *não* têm que produzir um **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="36d88-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="36d88-107">Por exemplo, "SHAPE {DROP TABLE MyTable} é um comando shape perfeitamente válido, desde que o provedor de dados ofereça suporte para DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="36d88-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="36d88-108">Essa capacidade permite que ambos os comandos normais de provedor e de shape compartilhem a mesma conexão e a mesma transação.</span><span class="sxs-lookup"><span data-stu-id="36d88-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

