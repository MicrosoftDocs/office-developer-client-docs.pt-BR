---
title: Propriedade NumericScale (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4229a318c4eb855b86164f02f1075d29a915d718
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464209"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="bd0d1-102">Propriedade NumericScale (ADOX)</span><span class="sxs-lookup"><span data-stu-id="bd0d1-102">NumericScale Property (ADOX)</span></span>


<span data-ttu-id="bd0d1-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd0d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bd0d1-104">Indica a escala de um valor numérico na coluna.</span><span class="sxs-lookup"><span data-stu-id="bd0d1-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="bd0d1-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="bd0d1-105">Settings and Return Values</span></span>

<span data-ttu-id="bd0d1-p101">Define e retorna um valor **Byte** que é a escala de valores de dados na coluna quando a propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) é **adNumeric** ou **adDecimal**. **NumericScale** é ignorado em todos os outros tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="bd0d1-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd0d1-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd0d1-108">Remarks</span></span>

<span data-ttu-id="bd0d1-109">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="bd0d1-109">The default value is zero (0).</span></span>

<span data-ttu-id="bd0d1-110">**NumericScale** é somente leitura em objetos [Column](column-object-adox.md) já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="bd0d1-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

