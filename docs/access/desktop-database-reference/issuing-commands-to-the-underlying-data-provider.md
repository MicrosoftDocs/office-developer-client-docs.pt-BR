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
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Emitindo comandos para o provedor de dados adjacente


**Aplica-se a**: Access 2013, o Office 2013

Qualquer comando que não comece com SHAPE passou pelo provedor de dados. Isso equivale à emissão de um comando shape no formulário "SHAPE {provider command}". Execute estes comandos *não* têm que produzir um **Recordset**. Por exemplo, "SHAPE {DROP TABLE MyTable} é um comando shape perfeitamente válido, desde que o provedor de dados ofereça suporte para DROP TABLE.

Essa capacidade permite que ambos os comandos normais de provedor e de shape compartilhem a mesma conexão e a mesma transação.

