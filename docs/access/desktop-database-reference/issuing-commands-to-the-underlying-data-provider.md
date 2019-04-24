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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291085"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Emissão de comandos para o provedor de dados subjacente

**Aplica-se ao:** Access 2013, Office 2013

Qualquer comando que não comece com SHAPE passou pelo provedor de dados. Isso equivale à emissão de um comando shape no formulário "SHAPE {provider command}". Esses comandos *não* têm como criar um **Recordset**. Por exemplo, "SHAPE {DROP TABLE MyTable} é um comando shape perfeitamente válido, desde que o provedor de dados ofereça suporte para DROP TABLE.

Essa capacidade permite que ambos os comandos normais de provedor e de shape compartilhem a mesma conexão e a mesma transação.

