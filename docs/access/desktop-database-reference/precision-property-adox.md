---
title: Propriedade Precision (ADOX)
TOCTitle: Precision Property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5fab2a7dc7a2d9f05e22b064acfaeabf93106a3e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462381"
---
# <a name="precision-property-adox"></a>Propriedade Precision (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Indica a precisão máxima dos valores de dados na coluna.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define e retorna um valor **Long** que é a precisão máxima dos valores de dados na coluna quando a propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) é um tipo numérico. **Precision** é ignorado em todos os outros tipos de dados.

## <a name="remarks"></a>Comentários

O valor padrão é zero (0).

Esta propriedade é somente leitura em objetos [Column](column-object-adox.md) já acrescentados a uma coleção.

