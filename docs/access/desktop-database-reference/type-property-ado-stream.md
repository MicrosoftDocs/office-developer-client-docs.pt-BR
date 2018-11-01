---
title: Propriedade Type (Stream do ADO)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a1101742e8c82b0eebcb0d260825f01905cb92a0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868725"
---
# <a name="type-property-ado-stream"></a>Propriedade Type (Stream do ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o tipo de dados contido no [Stream](stream-object-ado.md) (binário ou texto).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [StreamTypeEnum](streamtypeenum.md) que especifica o tipo de dados contido no objeto **Stream**. O valor padrão é **adTypeText**. Entretanto, se os dados binários forem inicialmente gravados em um **Stream** novo e vazio, a propriedade **Type** será alterada para **adTypeBinary**.

## <a name="remarks"></a>Comentários

A propriedade **Type** será leitura/gravação somente quando a posição atual estiver no início do **Stream** ([Position](position-property-ado.md) for 0) e somente leitura em qualquer outra posição.

A propriedade **Type** determina quais métodos devem ser utilizados para a leitura e gravação do **Stream**. Para os **Streams** de texto, utilize [ReadText](readtext-method-ado.md) e [WriteText](writetext-method-ado.md). Para **Streams** binários, utilize [Read](read-method-ado.md) e [Write](write-method-ado.md).

