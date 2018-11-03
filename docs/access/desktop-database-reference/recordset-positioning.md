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
# <a name="recordset-positioning"></a><span data-ttu-id="0d13c-102">Posicionamento no Recordset</span><span class="sxs-lookup"><span data-stu-id="0d13c-102">Recordset positioning</span></span>


<span data-ttu-id="0d13c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d13c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d13c-p101">Use a propriedade **AbsolutePosition** para mover um registro, de acordo com sua posição ordinal no objeto **Recordset** ou para determinar a posição ordinal do registro atual. O provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="0d13c-p101">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="0d13c-p102">**AbsolutePosition** é baseada em 1e igual a 1 quando o registro atual for o primeiro registro no **Recordset**. Conforme mencionado anteriormente, você poderá obter o número total de registros no objeto **Recordset** a partir da propriedade **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="0d13c-p102">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="0d13c-p103">Quando você define a propriedade **AbsolutePosition**, mesmo que seja para um registro no cache atual, o ADO recarrega o cache com um novo grupo de registros iniciando com o registro especificado. A propriedade **CacheSize** determina o tamanho desse grupo.</span><span class="sxs-lookup"><span data-stu-id="0d13c-p103">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The **CacheSize** property determines the size of this group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0d13c-p104">[!OBSERVAçãO] A propriedade <STRONG>AbsolutePosition</STRONG> não deve ser usada como um número de registro substituto. A posição de um dado registro é alterada quando você exclui um registro anterior. Também não existe garantia de que um dado registro terá a mesma propriedade <STRONG>AbsolutePosition</STRONG> se o objeto <STRONG>Recordset</STRONG> for reaberto ou consultado novamente. Os indicadores são a forma recomendada de reter e retornar a uma dada posição e são a única forma de se posicionar por todos os tipos de objetos <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0d13c-p104">You should not use the <STRONG>AbsolutePosition</STRONG> property as a surrogate record number. The position of a given record changes when you delete a preceding record. There also is no assurance that a given record will have the same <STRONG>AbsolutePosition</STRONG> if the <STRONG>Recordset</STRONG> object is requeried or reopened. Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <STRONG>Recordset</STRONG> objects.</span></span></P>


