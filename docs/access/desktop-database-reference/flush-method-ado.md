---
title: Método Flush - ActiveX Data Objects (ADO)
TOCTitle: Flush method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a55eb66c454d510d53083c495326548eda08af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292339"
---
# <a name="flush-method-ado"></a>Método Flush (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Força que o com que o conteúdo do [Stream](stream-object-ado.md) remanescente no buffer do ADO vá para o objeto base com o qual o **Stream** está associado.

## <a name="syntax"></a>Sintaxe

*Stream*. Flush

## <a name="remarks"></a>Comentários

Este método pode ser utilizado para enviar o conteúdo do buffer do fluxo para o objeto base (por exemplo, o nó ou arquivo representado pela URL que é a fonte do objeto **Stream** ). Este método deve ser chamado quando você deseja assegurar que todas as alterações feitas no conteúdo de um **Stream** sejam gravadas. No entanto, com o ADO, geralmente não é necessário chamar **Flush**, pois o ADO esvazia continuamente seu buffer o tanto quanto possível em segundo plano. As alterações no conteúdo de um **Stream** são feitas automaticamente, não armazenadas em cache até que **Flush** seja chamado.

Fechar um **Stream** com o método [Close](close-method-ado.md) esvazia automaticamente o conteúdo de um **Stream**; não há necessidade em chamar explicitamente **Flush** imediatamente antes de **Close**.

