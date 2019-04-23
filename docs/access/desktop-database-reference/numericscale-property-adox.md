---
title: Propriedade NumericScale (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288515"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="c829a-102">Propriedade NumericScale (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c829a-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="c829a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c829a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c829a-104">Indica a escala de um valor numérico na coluna.</span><span class="sxs-lookup"><span data-stu-id="c829a-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c829a-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c829a-105">Settings and return values</span></span>

<span data-ttu-id="c829a-p101">Define e retorna um valor **Byte** que é a escala de valores de dados na coluna quando a propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) é **adNumeric** ou **adDecimal**. **NumericScale** é ignorado em todos os outros tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="c829a-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="c829a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c829a-108">Remarks</span></span>

<span data-ttu-id="c829a-109">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="c829a-109">The default value is zero (0).</span></span>

<span data-ttu-id="c829a-110">**NumericScale** é somente leitura em objetos [Column](column-object-adox.md) já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="c829a-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

