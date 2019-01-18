---
title: Propriedade NumericScale (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bcb0c1a38108fbd02551df2a3296abe4d9a3791
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707102"
---
# <a name="numericscale-property-ado"></a><span data-ttu-id="dfa74-102">Propriedade NumericScale (ADO)</span><span class="sxs-lookup"><span data-stu-id="dfa74-102">NumericScale property (ADO)</span></span>


<span data-ttu-id="dfa74-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfa74-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dfa74-104">Indica a escala de valores numéricos em um objeto [Parameter](parameter-object-ado.md) ou [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dfa74-104">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="dfa74-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="dfa74-105">Settings and return values</span></span>

<span data-ttu-id="dfa74-106">Define ou retorna um valor **Byte** que indica o número de casas decimais para as quais os valores numéricos serão resolvidos.</span><span class="sxs-lookup"><span data-stu-id="dfa74-106">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfa74-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfa74-107">Remarks</span></span>

<span data-ttu-id="dfa74-108">Use a propriedade **NumericScale** para determinar quantos dígitos à direita da vírgula decimal serão usados para representar valores de um objeto numérico **Parameter** ou **Field**.</span><span class="sxs-lookup"><span data-stu-id="dfa74-108">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="dfa74-109">Em objetos **Parameter**, a propriedade **NumericScale** é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="dfa74-109">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="dfa74-p101">Em um objeto **Field**, **NumericScale** normalmente é somente leitura. No entanto, para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **NumericScale** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para o **Field** for especificada e o provedor de dados tiver adicionado com sucesso o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="dfa74-p101">For a **Field** object, **NumericScale** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

