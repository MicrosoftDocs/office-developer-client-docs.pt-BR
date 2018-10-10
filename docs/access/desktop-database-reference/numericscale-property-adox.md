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
# <a name="numericscale-property-adox"></a>Propriedade NumericScale (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Indica a escala de um valor numérico na coluna.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define e retorna um valor **Byte** que é a escala de valores de dados na coluna quando a propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) é **adNumeric** ou **adDecimal**. **NumericScale** é ignorado em todos os outros tipos de dados.

## <a name="remarks"></a>Comentários

O valor padrão é zero (0).

**NumericScale** é somente leitura em objetos [Column](column-object-adox.md) já acrescentados a uma coleção.

