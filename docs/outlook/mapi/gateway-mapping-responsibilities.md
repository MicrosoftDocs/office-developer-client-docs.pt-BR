---
title: Responsabilidades de mapeamento do gateway
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422751"
---
# <a name="gateway-mapping-responsibilities"></a>Responsabilidades de mapeamento do gateway

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um gateway que reconhece MAPI recebe uma mensagem contendo propriedades nomeadas em um dos conjuntos de propriedades especiais designados para conter propriedades mapeáveis de gateway, o gateway deve mapear todas as propriedades para o protocolo do sistema de mensagens de destino. Embora o MAPI recomende que os gateways manipularem todas as propriedades nomeadas nos conjuntos de propriedades especiais, espera-se que os gateways manipularão apenas dois: endereço de email e tipo de endereço. Como as propriedades do endereço de email e do tipo de endereço afetam diretamente a transmissão de mensagens, é fundamental que os gateways deem suporte ao mapeamento dessas duas propriedades. Como as chaves de pesquisa consistem no tipo de endereço e no endereço de um usuário, elas também devem ser traduzidas, se possível.
  
Não se espera que os identificadores de entrada sejam manipulados com frequência. Para habilitar o mapeamento de um identificador de entrada originado em um sistema de mensagens para um identificador de entrada que possa ser usado por outro sistema de mensagens, o gateway deve ser capaz de usar o formato dos dois sistemas. Como a maioria dos gateways não reconhece formatos de identificador de entrada, a tradução dos identificadores de entrada é rara.
  
Outra propriedade mappable que não se espera que seja traduzida com frequência é o nome de exibição. Gateways devem armazenar nomes de exibição e transmiti-los, mas não necessariamente traduzi-los. 
  

