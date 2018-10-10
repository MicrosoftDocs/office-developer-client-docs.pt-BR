---
title: Propriedade InternetTimeout (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929b166a308276836fbe4a48a2461ef7eb0caba2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461981"
---
# <a name="internettimeout-property-rds"></a>Propriedade InternetTimeout (RDS)


**Aplica-se a**: Access 2013 | Office 2013

Indica o tempo de espera, em milissegundos, antes do tempo limite de uma solicitação.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que representa o número de milissegundos antes do tempo limite de uma solicitação.

## <a name="remarks"></a>Comentários

Esta propriedade aplica-se apenas às solicitações enviadas com os protocolos HTTP ou HTTPS.

Solicitações em um ambiente de três camadas podem demorar alguns minutos para serem executadas. Use esta propriedade para especificar o tempo adicional para solicitações longas.

