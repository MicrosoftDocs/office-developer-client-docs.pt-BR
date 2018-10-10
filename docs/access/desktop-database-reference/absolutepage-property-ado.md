---
title: Propriedade AbsolutePage (ADO)
TOCTitle: AbsolutePage Property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 60b7b58efaa6fb8686e4f43da9b9733f3629f1a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464336"
---
# <a name="absolutepage-property-ado"></a><span data-ttu-id="3d019-102">Propriedade AbsolutePage (ADO)</span><span class="sxs-lookup"><span data-stu-id="3d019-102">AbsolutePage Property (ADO)</span></span>


<span data-ttu-id="3d019-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d019-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3d019-104">Indica a página na qual está o registro atual.</span><span class="sxs-lookup"><span data-stu-id="3d019-104">Indicates on which page the current record resides.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3d019-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3d019-105">Settings and Return Values</span></span>

<span data-ttu-id="3d019-106">Define ou retorna um valor **Long** de 1 até o número de páginas no objeto [Recordset](recordset-object-ado.md) ( [PageCount](pagecount-property-ado.md)) ou retorna um dos valores [PositionEnum](positionenum.md).</span><span class="sxs-lookup"><span data-stu-id="3d019-106">Sets or returns a **Long** value from 1 to the number of pages in the [Recordset](recordset-object-ado.md) object ( [PageCount](pagecount-property-ado.md) ), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d019-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d019-107">Remarks</span></span>

<span data-ttu-id="3d019-p101">Essa propriedade pode ser usada para identificar o número da página na qual o registro atual está localizado. Ela usa a propriedade [PageSize](pagesize-property-ado.md) para dividir de modo lógico a contagem total do conjunto de linhas do objeto **Recordset** em uma série de páginas, cada qual com um número de registros equivalente à **PageSize** (exceto a última página, que pode conter um número menor de registros). O provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="3d019-p101">This property can be used to identify the page number on which the current record is located. It uses the [PageSize](pagesize-property-ado.md) property to logically divide the total rowset count of the **Recordset** object into a series of pages, each of which has the number of records equal to **PageSize** (except for the last page, which may have fewer records). The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="3d019-111">Ao obter ou configurar a propriedade **AbsolutePage**, o ADO usa as propriedades [AbsolutePosition](absoluteposition-property-ado.md) e [PageSize](pagesize-property-ado.md) conjuntamente conforme se segue:</span><span class="sxs-lookup"><span data-stu-id="3d019-111">When getting or setting the **AbsolutePage** property, ADO uses the [AbsolutePosition](absoluteposition-property-ado.md) property and the [PageSize](pagesize-property-ado.md) property together as follows:</span></span>

  - <span data-ttu-id="3d019-112">Para obter a **AbsolutePage**, o ADO primeiro recupera a **AbsolutePosition** e a divide pela **PageSize**.</span><span class="sxs-lookup"><span data-stu-id="3d019-112">To get the **AbsolutePage**, ADO first retrieves the **AbsolutePosition**, and then divides it by the **PageSize**.</span></span>

  - <span data-ttu-id="3d019-p102">Para definir a **AbsolutePage**, o ADO move a **AbsolutePosition** da seguinte maneira: ele multiplica a **PageSize** pelo novo valor da **AbsolutePage** e acrescenta 1 ao valor. Como resultado, a posição atual no **Recordset** após a configuração bem-sucedida da **AbsolutePage** é o primeiro registro daquela página.</span><span class="sxs-lookup"><span data-stu-id="3d019-p102">To set the **AbsolutePage**, ADO moves the **AbsolutePosition** as follows: it multiplies the **PageSize** by the new **AbsolutePage** value and then adds 1 to the value. As a result, the current position in the **Recordset** after successfully setting **AbsolutePage** is, the first record in that page.</span></span>

<span data-ttu-id="3d019-p103">Da mesma forma que a propriedade **AbsolutePosition**, a **AbsolutePage** tem base unitária e equivale a 1 quando o registro atual é o primeiro registro no **Recordset**. Defina essa propriedade para mover para o primeiro registro de uma página específica. Obtenha o número total de páginas da propriedade **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="3d019-p103">Like the **AbsolutePosition** property, **AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

