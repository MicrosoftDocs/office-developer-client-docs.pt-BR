---
title: Propriedade DateCreated (ADOX)
TOCTitle: DateCreated Property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 962c5e00eee3c58d2c02040869fdf1cb454af538
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464326"
---
# <a name="datecreated-property-adox"></a>Propriedade DateCreated (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Indica a data de criação do objeto.

## <a name="return-values"></a>Valores de retorno

Retorna um valor **Variant** que especifica a data de criação. O valor será nulo se o provedor não oferecer suporte a **DateCreated**.

## <a name="remarks"></a>Comentários

A propriedade **DateCreated** é nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateCreated**.

