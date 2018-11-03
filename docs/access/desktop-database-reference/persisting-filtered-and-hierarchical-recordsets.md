---
title: Mantendo Recordsets hierárquicos e filtrados
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13255bcd5cd40745a767b8aff9f49449b0127294
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946115"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Mantendo Recordsets hierárquicos e filtrados


**Aplica-se a**: Access 2013, o Office 2013

Se a propriedade [Filter](filter-property-ado.md) estiver em vigor para o **Recordset**, somente as linhas acessíveis sob o filtro serão salvas. Se o **Recordset** for hierárquico, o **Recordset** filho e seus filhos serão salvos, incluindo o **Recordset** pai. Se o método **Save** de um **Recordset** filho for chamado, o filho e todos seus filhos serão salvos, mas o pai não será. Para obter mais informações sobre **Recordsets** hierárquicos, consulte o [Capítulo 9: Data Shaping](chapter-9-data-shaping.md).


> [!NOTE]
> [!OBSERVAçãO] Algumas limitações se aplicam ao salvar **Recordsets** hierárquicos (formas de dados) em formato XML. Para obter mais informações, consulte [Recordsets hierárquicos em XML](hierarchical-recordsets-in-xml.md).


