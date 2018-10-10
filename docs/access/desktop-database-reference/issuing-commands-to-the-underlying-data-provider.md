---
title: Emitindo comandos para o provedor de dados adjacente
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083f339860e0b28b43e2ceefeaf2cdd1de4b660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463045"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="30817-102">Emitindo comandos para o provedor de dados adjacente</span><span class="sxs-lookup"><span data-stu-id="30817-102">Issuing Commands to the Underlying Data Provider</span></span>


<span data-ttu-id="30817-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="30817-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="30817-104">Qualquer comando que não comece com SHAPE passou pelo provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="30817-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="30817-105">Isso equivale à emissão de um comando shape no formulário "SHAPE {provider command}".</span><span class="sxs-lookup"><span data-stu-id="30817-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="30817-106">Execute estes comandos *não* têm que produzir um **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="30817-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="30817-107">Por exemplo, "SHAPE {DROP TABLE MyTable} é um comando shape perfeitamente válido, desde que o provedor de dados ofereça suporte para DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="30817-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="30817-108">Essa capacidade permite que ambos os comandos normais de provedor e de shape compartilhem a mesma conexão e a mesma transação.</span><span class="sxs-lookup"><span data-stu-id="30817-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

