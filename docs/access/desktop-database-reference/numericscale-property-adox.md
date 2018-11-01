---
title: Propriedade NumericScale (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11696e379fe618f07a6087eee26ba21a2d27b3e5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890915"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="3601e-102">Propriedade NumericScale (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3601e-102">NumericScale Property (ADOX)</span></span>


<span data-ttu-id="3601e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3601e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3601e-104">Indica a escala de um valor numérico na coluna.</span><span class="sxs-lookup"><span data-stu-id="3601e-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3601e-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3601e-105">Settings and return values</span></span>

<span data-ttu-id="3601e-p101">Define e retorna um valor **Byte** que é a escala de valores de dados na coluna quando a propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) é **adNumeric** ou **adDecimal**. **NumericScale** é ignorado em todos os outros tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="3601e-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="3601e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3601e-108">Remarks</span></span>

<span data-ttu-id="3601e-109">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="3601e-109">The default value is zero (0).</span></span>

<span data-ttu-id="3601e-110">**NumericScale** é somente leitura em objetos [Column](column-object-adox.md) já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="3601e-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

