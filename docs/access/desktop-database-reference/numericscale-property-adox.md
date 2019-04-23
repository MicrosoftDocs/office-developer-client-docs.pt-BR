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
# <a name="numericscale-property-adox"></a>Propriedade NumericScale (ADOX)


**Aplica-se ao:** Access 2013, Office 2013

Indica a escala de um valor numérico na coluna.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define e retorna um valor **Byte** que é a escala de valores de dados na coluna quando a propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) é **adNumeric** ou **adDecimal**. **NumericScale** é ignorado em todos os outros tipos de dados.

## <a name="remarks"></a>Comentários

O valor padrão é zero (0).

**NumericScale** é somente leitura em objetos [Column](column-object-adox.md) já acrescentados a uma coleção.

