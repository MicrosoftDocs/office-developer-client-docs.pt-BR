---
title: Propriedade Precision (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 662e5e9287da1ccfb81c727f5d5e5dfedce2969b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287472"
---
# <a name="precision-property-ado"></a><span data-ttu-id="4e52c-102">Propriedade Precision (ADO)</span><span class="sxs-lookup"><span data-stu-id="4e52c-102">Precision property (ADO)</span></span>


<span data-ttu-id="4e52c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e52c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e52c-104">Indica o grau de precisão de valores numéricos em um objeto [Parameter](parameter-object-ado.md) ou de objetos [Field](field-object-ado.md) numéricos.</span><span class="sxs-lookup"><span data-stu-id="4e52c-104">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4e52c-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="4e52c-105">Settings and return values</span></span>

<span data-ttu-id="4e52c-106">Define ou retorna um valor **Byte** que indica o número máximo de dígitos utilizado para representar os valores.</span><span class="sxs-lookup"><span data-stu-id="4e52c-106">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e52c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e52c-107">Remarks</span></span>

<span data-ttu-id="4e52c-108">Utilize a propriedade **Precision** para determinar o número máximo de dígitos utilizado para representar os valores de um objeto numérico **Parameter** ou **Field**.</span><span class="sxs-lookup"><span data-stu-id="4e52c-108">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="4e52c-109">O valor é leitura/gravação em um objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="4e52c-109">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="4e52c-p101">Para um objeto **Field**, a propriedade **Precision** normalmente é somente leitura. Entretanto, para novos objetos **Field** que tenham sido acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Precision** será leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) de **Field** tiver sido especificada e o provedor de dados tiver adicionado com êxito o novo **Field** por meio da chamada do método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="4e52c-p101">For a **Field** object, **Precision** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

