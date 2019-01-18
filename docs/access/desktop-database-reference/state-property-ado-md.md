---
title: Propriedade State (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702443"
---
# <a name="state-property-ado-md"></a>Propriedade State (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica o estado atual do conjunto de células.

## <a name="return-values"></a>Valores de retorno

Retorna um inteiro **Long** que indica a condição atual do objeto [Cellset](cellset-object-ado-md.md) e é somente leitura. Os seguintes valores são válidos: **adStateClosed** (0) e **adStateOpen** (1).

## <a name="remarks"></a>Comentários

Para usar os nomes da constante [ObjectStateEnum](objectstateenum.md), a biblioteca de tipos ADO deve ser referenciada em seu projeto. Para obter mais informações, consulte [Usando o ADO com o ADO MD](using-ado-with-ado-md.md).

