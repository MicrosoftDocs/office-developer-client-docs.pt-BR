---
title: Propriedade State (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722820"
---
# <a name="state-property-ado"></a>Propriedade State (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica todos os objetos aplicáveis, independentemente de seu estado: aberto ou fechado.

Indica todos os objetos aplicáveis que executam um método assíncrono, independentemente de seu estado atual: conexão, execução ou recuperação.

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long** que pode ser um valor [ObjectStateEnum](objectstateenum.md). O valor padrão é **adStateClosed**.

## <a name="remarks"></a>Comentários

Você pode utilizar a propriedade **State** para identificar o estado atual de um determinado objeto em qualquer momento.

A propriedade **State** do objeto pode ter uma combinação de valores. Por exemplo, se uma instrução estiver sendo executada, essa propriedade terá uma combinação de valores de **adStateOpen** e **adStateExecuting**.

A propriedade **State** é somente leitura.

