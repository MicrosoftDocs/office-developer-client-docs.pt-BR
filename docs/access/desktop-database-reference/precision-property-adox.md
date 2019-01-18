---
title: Propriedade Precision (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f05f6880a9599421189519f263cfb27bf1432325
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726159"
---
# <a name="precision-property-adox"></a>Propriedade Precision (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Indica a precisão máxima dos valores de dados na coluna.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define e retorna um valor **Long** que é a precisão máxima dos valores de dados na coluna quando a propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) é um tipo numérico. **Precision** é ignorado em todos os outros tipos de dados.

## <a name="remarks"></a>Comentários

O valor padrão é zero (0).

Esta propriedade é somente leitura em objetos [Column](column-object-adox.md) já acrescentados a uma coleção.

