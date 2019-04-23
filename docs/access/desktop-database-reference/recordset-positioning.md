---
title: Posicionamento do conjunto de registros
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cffb5adce1266bd7fdd08989e9f92110f4829ba0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284501"
---
# <a name="recordset-positioning"></a><span data-ttu-id="caa1a-102">Posicionamento do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="caa1a-102">Recordset positioning</span></span>

<span data-ttu-id="caa1a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="caa1a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="caa1a-p101">Use a propriedade **AbsolutePosition** para mover um registro, de acordo com sua posição ordinal no objeto **Recordset** ou para determinar a posição ordinal do registro atual. O provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="caa1a-p101">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="caa1a-p102">**AbsolutePosition** é baseada em 1e igual a 1 quando o registro atual for o primeiro registro no **Recordset**. Conforme mencionado anteriormente, você poderá obter o número total de registros no objeto **Recordset** a partir da propriedade **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="caa1a-p102">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="caa1a-p103">Quando você define a propriedade **AbsolutePosition**, mesmo que seja para um registro no cache atual, o ADO recarrega o cache com um novo grupo de registros iniciando com o registro especificado. A propriedade **CacheSize** determina o tamanho desse grupo.</span><span class="sxs-lookup"><span data-stu-id="caa1a-p103">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The **CacheSize** property determines the size of this group.</span></span>

> [!NOTE]
> <span data-ttu-id="caa1a-p104">[!OBSERVAçãO] A propriedade **AbsolutePosition** não deve ser usada como um número de registro substituto. A posição de um dado registro é alterada quando você exclui um registro anterior. Também não existe garantia de que um dado registro terá a mesma propriedade **AbsolutePosition** se o objeto **Recordset** for reaberto ou consultado novamente. Os indicadores são a forma recomendada de reter e retornar a uma dada posição e são a única forma de se posicionar por todos os tipos de objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="caa1a-p104">You should not use the **AbsolutePosition** property as a surrogate record number. The position of a given record changes when you delete a preceding record. There also is no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened. Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of **Recordset** objects.</span></span>


