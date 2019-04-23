---
title: Propriedade AbsolutePosition (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b5e25e014c6e93d35e3621bb9b5b3c21d5e77f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281974"
---
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="79da4-102">Propriedade AbsolutePosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="79da4-102">AbsolutePosition property (ADO)</span></span>

<span data-ttu-id="79da4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79da4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79da4-104">Indica a posição ordinal do registro atual de um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="79da4-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="79da4-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="79da4-105">Settings and return values</span></span>

<span data-ttu-id="79da4-106">Define ou retorna um valor **Long** de 1 até o número de registros no objeto **Recordset**  ([RecordCount](recordcount-property-ado.md)) ou retorna um dos valores [PositionEnum](positionenum.md).</span><span class="sxs-lookup"><span data-stu-id="79da4-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="79da4-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="79da4-107">Remarks</span></span>

<span data-ttu-id="79da4-108">Para definir a propriedade **AbsolutePosition** , o ADO requer que o provedor OLE DB que você está usando implemente a interface IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="79da4-108">To set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="79da4-p101">O acesso à propriedade **AbsolutePosition** de um **Recordset** aberto usando um cursor somente de encaminhamento ou dinâmico provoca o erro **adErrFeatureNotAvailable**. Com outros tipos de cursor, a posição correta será retornada, desde que o provedor ofereça suporte à interface IRowsetScroll. Se o provedor não oferecer suporte a essa *interface*, a propriedade será definida como **adPosUnknown**. Consulte a documentação do seu provedor para identificar se ele oferece suporte à *IRowsetScroll*.</span><span class="sxs-lookup"><span data-stu-id="79da4-p101">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**. See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="79da4-p102">Use a propriedade **AbsolutePosition** para mover um registro, de acordo com sua posição ordinal no objeto **Recordset** ou para determinar a posição ordinal do registro atual. O provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="79da4-p102">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="79da4-p103">Assim como a propriedade [AbsolutePage](absolutepage-property-ado.md), **AbsolutePosition** tem base unitária e equivale a 1 quando o registro atual é o primeiro registro no **Recordset**. É possível obter o número total de registros no objeto **Recordset** usando a propriedade [RecordCount](recordcount-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="79da4-p103">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="79da4-117">Quando você define a propriedade **AbsolutePosition** , mesmo que seja um registro no cache atual, o ADO recarrega o cache com um novo grupo de registros começando com o registro que você especificou.</span><span class="sxs-lookup"><span data-stu-id="79da4-117">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record that you specified.</span></span> <span data-ttu-id="79da4-118">A propriedade [CacheSize](cachesize-property-ado.md) determina o tamanho desse grupo.</span><span class="sxs-lookup"><span data-stu-id="79da4-118">The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <span data-ttu-id="79da4-119">[!OBSERVAçãO] A propriedade **AbsolutePosition** não deve ser usada como um número de registro substituto.</span><span class="sxs-lookup"><span data-stu-id="79da4-119">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="79da4-120">A posição de um determinado registro é alterada quando um registro precedente é excluído.</span><span class="sxs-lookup"><span data-stu-id="79da4-120">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="79da4-121">Também não há garantias de que um determinado registro terá a mesma **AbsolutePosition** se o objeto **Recordset** for consultado e aberto novamente.</span><span class="sxs-lookup"><span data-stu-id="79da4-121">There is also no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="79da4-122">Os indicadores ainda são a forma recomendada de reter e retornar a uma determinada posição e são a única maneira de posicionar em todos os tipos de objetos **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="79da4-122">Bookmarks are still the recommended way of retaining and returning to a given position, and are the only way of positioning across all types of **Recordset** objects.</span></span>


