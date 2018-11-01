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
# <a name="numericscale-property-adox"></a>Propriedade NumericScale (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Indica a escala de um valor numérico na coluna.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define e retorna um valor **Byte** que é a escala de valores de dados na coluna quando a propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) é **adNumeric** ou **adDecimal**. **NumericScale** é ignorado em todos os outros tipos de dados.

## <a name="remarks"></a>Comentários

O valor padrão é zero (0).

**NumericScale** é somente leitura em objetos [Column](column-object-adox.md) já acrescentados a uma coleção.

