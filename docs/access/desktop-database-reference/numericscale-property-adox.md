---
title: Propriedade NumericScale (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1a15f78463ca0ff6e690b600b9cdca7cc194c7
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025956"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="e3574-102">Propriedade NumericScale (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e3574-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="e3574-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3574-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3574-104">Indica a escala de um valor numérico na coluna.</span><span class="sxs-lookup"><span data-stu-id="e3574-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e3574-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="e3574-105">Settings and return values</span></span>

<span data-ttu-id="e3574-p101">Define e retorna um valor **Byte** que é a escala de valores de dados na coluna quando a propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) é **adNumeric** ou **adDecimal**. **NumericScale** é ignorado em todos os outros tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="e3574-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3574-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3574-108">Remarks</span></span>

<span data-ttu-id="e3574-109">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="e3574-109">The default value is zero (0).</span></span>

<span data-ttu-id="e3574-110">**NumericScale** é somente leitura em objetos [Column](column-object-adox.md) já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="e3574-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

