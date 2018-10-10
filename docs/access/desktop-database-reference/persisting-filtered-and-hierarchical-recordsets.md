---
title: Mantendo recordsets hierárquicos e filtrados
TOCTitle: Persisting Filtered and Hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d29fe867933bdff93d064a95a4fc95c65e8605f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463098"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Mantendo recordsets hierárquicos e filtrados


**Aplica-se a**: Access 2013 | Office 2013

Se a propriedade [Filter](filter-property-ado.md) estiver em vigor para o **Recordset**, somente as linhas acessíveis sob o filtro serão salvas. Se o **Recordset** for hierárquico, o **Recordset** filho e seus filhos serão salvos, incluindo o **Recordset** pai. Se o método **Save** de um **Recordset** filho for chamado, o filho e todos seus filhos serão salvos, mas o pai não será. Para obter mais informações sobre **Recordsets** hierárquicos, consulte o [Capítulo 9: Data Shaping](chapter-9-data-shaping.md).


> [!NOTE]
> <P>[!OBSERVAçãO] Algumas limitações se aplicam ao salvar <STRONG>Recordsets</STRONG> hierárquicos (formas de dados) em formato XML. Para obter mais informações, consulte <A href="hierarchical-recordsets-in-xml.md">Recordsets hierárquicos em XML</A>.</P>


