---
title: Propriedade InternetTimeout (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1287289de5ef303e41a342ef84822d3a14083470
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918804"
---
# <a name="internettimeout-property-rds"></a>Propriedade InternetTimeout (RDS)


**Aplica-se a**: Access 2013, o Office 2013

Indica o tempo de espera, em milissegundos, antes do tempo limite de uma solicitação.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que representa o número de milissegundos antes do tempo limite de uma solicitação.

## <a name="remarks"></a>Comentários

Esta propriedade aplica-se apenas às solicitações enviadas com os protocolos HTTP ou HTTPS.

Solicitações em um ambiente de três camadas podem demorar alguns minutos para serem executadas. Use esta propriedade para especificar o tempo adicional para solicitações longas.

