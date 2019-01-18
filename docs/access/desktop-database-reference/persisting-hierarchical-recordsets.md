---
title: Conjuntos de registros hierárquicos persistentes
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1964d207f2b35eaeaf51b409adc12a41eac6438f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718606"
---
# <a name="persisting-hierarchical-recordsets"></a>Conjuntos de registros hierárquicos persistentes

**Aplica-se a**: Access 2013, o Office 2013

Você pode salvar um **Recordset** hierárquico em um arquivo tanto no formato ADTG quanto XML, chamando o método [Save](save-method-ado.md). Contudo, duas limitações se aplicam ao salvar **Recordset**s hierárquicos no formato XML: você não pode salvar em XML se o **Recordset** hierárquico contiver atualizações pendentes e nem salvar um **Recordset** hierárquico parametrizado.

Para obter mais informações sobre o provedor de Forma de dados, consulte [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) e o Serviço de forma de dados para OLE DB (OLE DB).

