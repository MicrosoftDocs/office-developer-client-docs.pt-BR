---
title: Posicionamento no Recordset
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5116adbf68e4e98c7fbda8285348e00638465742
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946269"
---
# <a name="recordset-positioning"></a>Posicionamento no Recordset


**Aplica-se a**: Access 2013, o Office 2013

Use a propriedade **AbsolutePosition** para mover um registro, de acordo com sua posição ordinal no objeto **Recordset** ou para determinar a posição ordinal do registro atual. O provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.

**AbsolutePosition** é baseada em 1e igual a 1 quando o registro atual for o primeiro registro no **Recordset**. Conforme mencionado anteriormente, você poderá obter o número total de registros no objeto **Recordset** a partir da propriedade **RecordCount**.

Quando você define a propriedade **AbsolutePosition**, mesmo que seja para um registro no cache atual, o ADO recarrega o cache com um novo grupo de registros iniciando com o registro especificado. A propriedade **CacheSize** determina o tamanho desse grupo.


> [!NOTE]
> <P>[!OBSERVAçãO] A propriedade <STRONG>AbsolutePosition</STRONG> não deve ser usada como um número de registro substituto. A posição de um dado registro é alterada quando você exclui um registro anterior. Também não existe garantia de que um dado registro terá a mesma propriedade <STRONG>AbsolutePosition</STRONG> se o objeto <STRONG>Recordset</STRONG> for reaberto ou consultado novamente. Os indicadores são a forma recomendada de reter e retornar a uma dada posição e são a única forma de se posicionar por todos os tipos de objetos <STRONG>Recordset</STRONG>.</P>


