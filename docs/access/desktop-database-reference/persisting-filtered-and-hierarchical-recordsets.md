---
title: Conjuntos de registros persistentes filtrados e hierárquicos
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1332d4348c993f94d8b2ee61280b8b35c02324c4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725942"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Conjuntos de registros persistentes filtrados e hierárquicos


**Aplica-se a**: Access 2013, o Office 2013

Se a propriedade [Filter](filter-property-ado.md) estiver em vigor para o **Recordset**, somente as linhas acessíveis sob o filtro serão salvas. Se o **Recordset** for hierárquico, o **Recordset** filho e seus filhos serão salvos, incluindo o **Recordset** pai. Se o método **Save** de um **Recordset** filho for chamado, o filho e todos seus filhos serão salvos, mas o pai não será. Para obter mais informações sobre **Recordsets** hierárquicos, consulte o [Capítulo 9: Data Shaping](chapter-9-data-shaping.md).


> [!NOTE]
> [!OBSERVAçãO] Algumas limitações se aplicam ao salvar **Recordsets** hierárquicos (formas de dados) em formato XML. Para obter mais informações, consulte [Recordsets hierárquicos em XML](hierarchical-recordsets-in-xml.md).


