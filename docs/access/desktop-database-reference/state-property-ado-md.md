---
title: Propriedade State (ADO MD)
TOCTitle: State Property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a42ade39a50eb5dc40e213d6f4c3f4ed0ba3475e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463440"
---
# <a name="state-property-ado-md"></a>Propriedade State (ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Indica o estado atual do conjunto de células.

## <a name="return-values"></a>Valores de retorno

Retorna um inteiro **Long** que indica a condição atual do objeto [Cellset](cellset-object-ado-md.md) e é somente leitura. Os seguintes valores são válidos: **adStateClosed** (0) e **adStateOpen** (1).

## <a name="remarks"></a>Comentários

Para usar os nomes da constante [ObjectStateEnum](objectstateenum.md), a biblioteca de tipos ADO deve ser referenciada em seu projeto. Para obter mais informações, consulte [Usando o ADO com o ADO MD](using-ado-with-ado-md.md).

