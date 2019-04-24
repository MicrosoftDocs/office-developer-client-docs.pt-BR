---
title: Propriedade InternetTimeout (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291238"
---
# <a name="internettimeout-property-rds"></a>Propriedade InternetTimeout (RDS)


**Aplica-se ao:** Access 2013, Office 2013

Indica o tempo de espera, em milissegundos, antes do tempo limite de uma solicitação.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que representa o número de milissegundos antes do tempo limite de uma solicitação.

## <a name="remarks"></a>Comentários

Esta propriedade aplica-se apenas às solicitações enviadas com os protocolos HTTP ou HTTPS.

Solicitações em um ambiente de três camadas podem demorar alguns minutos para serem executadas. Use esta propriedade para especificar o tempo adicional para solicitações longas.

