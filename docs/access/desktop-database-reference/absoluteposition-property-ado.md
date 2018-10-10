---
title: Propriedade AbsolutePosition (ADO)
TOCTitle: AbsolutePosition Property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3258ffcab87b16e4931c9881a8e8d1cd2143262f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464904"
---
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="85861-102">Propriedade AbsolutePosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="85861-102">AbsolutePosition Property (ADO)</span></span>


<span data-ttu-id="85861-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="85861-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="85861-104">Indica a posição ordinal do registro atual de um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="85861-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="85861-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="85861-105">Settings and Return Values</span></span>

<span data-ttu-id="85861-106">Define ou retorna um valor **Long** de 1 até o número de registros no objeto **Recordset**  ([RecordCount](recordcount-property-ado.md)) ou retorna um dos valores [PositionEnum](positionenum.md).</span><span class="sxs-lookup"><span data-stu-id="85861-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="85861-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="85861-107">Remarks</span></span>

<span data-ttu-id="85861-108">Para definir a propriedade **AbsolutePosition**, o ADO requer que o provedor OLE DB utilizado implemente a interface IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="85861-108">In order to set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="85861-p101">O acesso à propriedade **AbsolutePosition** de um **Recordset** aberto usando um cursor somente de encaminhamento ou dinâmico provoca o erro **adErrFeatureNotAvailable**. Com outros tipos de cursor, a posição correta será retornada, desde que o provedor ofereça suporte à interface IRowsetScroll. Se o provedor não oferecer suporte a essa *interface*, a propriedade será definida como **adPosUnknown**. Consulte a documentação do seu provedor para identificar se ele oferece suporte à *IRowsetScroll*.</span><span class="sxs-lookup"><span data-stu-id="85861-p101">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**. See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="85861-p102">Use a propriedade **AbsolutePosition** para mover um registro, de acordo com sua posição ordinal no objeto **Recordset** ou para determinar a posição ordinal do registro atual. O provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="85861-p102">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="85861-p103">Assim como a propriedade [AbsolutePage](absolutepage-property-ado.md), **AbsolutePosition** tem base unitária e equivale a 1 quando o registro atual é o primeiro registro no **Recordset**. É possível obter o número total de registros no objeto **Recordset** usando a propriedade [RecordCount](recordcount-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="85861-p103">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="85861-p104">Quando a propriedade **AbsolutePosition** é definida, mesmo que seja para um registro no cache atual, o ADO recarrega o cache com um novo grupo de registros, começando pelo registro especificado. A propriedade [CacheSize](cachesize-property-ado.md) determina o tamanho desse grupo.</span><span class="sxs-lookup"><span data-stu-id="85861-p104">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="85861-p105">[!OBSERVAçãO] Não se deve usar a propriedade <STRONG>AbsolutePosition</STRONG> como um número de registro substituto. A posição de um determinado registro é alterada quando um registro precedente é excluído. Também não há garantias de que um determinado registro terá a mesma <STRONG>AbsolutePosition</STRONG> se o objeto <STRONG>Recordset</STRONG> for consultado e aberto novamente. Os indicadores ainda são o modo recomendado para se reter e retornar a uma determinada posição e são o único modo de posicionamento presente em todos os tipos de objetos <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="85861-p105">You should not use the <STRONG>AbsolutePosition</STRONG> property as a surrogate record number. The position of a given record changes when you delete a preceding record. There is also no assurance that a given record will have the same <STRONG>AbsolutePosition</STRONG> if the <STRONG>Recordset</STRONG> object is requeried or reopened. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <STRONG>Recordset</STRONG> objects.</span></span></P>


