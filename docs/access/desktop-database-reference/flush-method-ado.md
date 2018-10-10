---
title: Liberar o método - ActiveX Data Objects (ADO)
TOCTitle: Flush Method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c2d7543d2e9a1229661e572e95b783621aa43fa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464868"
---
# <a name="flush-method-ado"></a>Método Flush (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Força que o com que o conteúdo do [Stream](stream-object-ado.md) remanescente no buffer do ADO vá para o objeto base com o qual o **Stream** está associado.

## <a name="syntax"></a>Sintaxe

*Stream*. Liberar

## <a name="remarks"></a>Comentários

Este método pode ser utilizado para enviar o conteúdo do buffer do fluxo para o objeto base (por exemplo, o nó ou arquivo representado pela URL que é a fonte do objeto **Stream** ). Este método deve ser chamado quando você deseja assegurar que todas as alterações feitas no conteúdo de um **Stream** sejam gravadas. No entanto, com o ADO, geralmente não é necessário chamar **Flush**, pois o ADO esvazia continuamente seu buffer o tanto quanto possível em segundo plano. As alterações no conteúdo de um **Stream** são feitas automaticamente, não armazenadas em cache até que **Flush** seja chamado.

Fechar um **Stream** com o método [Close](close-method-ado.md) esvazia automaticamente o conteúdo de um **Stream**; não há necessidade em chamar explicitamente **Flush** imediatamente antes de **Close**.

