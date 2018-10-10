---
title: Propriedade DateModified (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462297"
---
# <a name="datemodified-property-adox"></a>Propriedade DateModified (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Indica a data da última modificação do objeto.

## <a name="return-values"></a>Valores de retorno

Retorna um valor **Variant** que especifica a data de modificação. O valor será nulo se o provedor não oferecer suporte a **DateModified**.

## <a name="remarks"></a>Comentários

A propriedade **DateModified** será nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateModified**.

