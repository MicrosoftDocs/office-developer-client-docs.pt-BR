---
title: Propriedade State (ADO MD)
TOCTitle: State Property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bc1efc33aa263275ba50526ff682b64a229293f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885462"
---
# <a name="state-property-ado-md"></a>Propriedade State (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica o estado atual do conjunto de células.

## <a name="return-values"></a>Valor de retorno

Retorna um inteiro **Long** que indica a condição atual do objeto [Cellset](cellset-object-ado-md.md) e é somente leitura. Os seguintes valores são válidos: **adStateClosed** (0) e **adStateOpen** (1).

## <a name="remarks"></a>Comentários

Para usar os nomes da constante [ObjectStateEnum](objectstateenum.md), a biblioteca de tipos ADO deve ser referenciada em seu projeto. Para obter mais informações, consulte [Usando o ADO com o ADO MD](using-ado-with-ado-md.md).

