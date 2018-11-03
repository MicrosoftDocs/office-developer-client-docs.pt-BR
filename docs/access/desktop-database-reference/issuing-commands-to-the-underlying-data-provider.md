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
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Emitindo comandos para o provedor de dados subjacente

**Aplica-se a**: Access 2013, o Office 2013

Qualquer comando que não comece com SHAPE passou pelo provedor de dados. Isso equivale à emissão de um comando shape no formulário "SHAPE {provider command}". Execute estes comandos *não* têm que produzir um **Recordset**. Por exemplo, "SHAPE {DROP TABLE MyTable} é um comando shape perfeitamente válido, desde que o provedor de dados ofereça suporte para DROP TABLE.

Essa capacidade permite que ambos os comandos normais de provedor e de shape compartilhem a mesma conexão e a mesma transação.

