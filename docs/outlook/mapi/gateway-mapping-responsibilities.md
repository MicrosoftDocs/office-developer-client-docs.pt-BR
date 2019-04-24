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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342795"
---
# <a name="gateway-mapping-responsibilities"></a>Responsabilidades de mapeamento do gateway

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um gateway de reconhecimento MAPI recebe uma mensagem que contém propriedades nomeadas em um dos conjuntos de propriedades especiais designados para conter Propriedades do gateway-mapeáveis, o gateway deve mapear todas as propriedades para o protocolo do sistema de mensagens de destino. Embora a MAPI recomende que os gateways manipulem todas as propriedades nomeadas nos conjuntos de propriedades especiais, os gateways são esperados para lidar apenas com dois: endereço de email e tipo de endereço. Como o endereço de email e as propriedades de tipo de endereço afetam diretamente a transmissão de mensagens, é fundamental que os gateways ofereçam suporte ao mapeamento dessas duas propriedades. Como as chaves de pesquisa consistem em um tipo de endereço e endereço de um usuário, elas também devem ser traduzidas, se possível.
  
Os identificadores de entrada não devem ser manipulados com frequência. Para habilitar o mapeamento de um identificador de entrada que se origina em um sistema de mensagens para um identificador de entrada que pode ser usado por outro sistema de mensagens, o gateway deve ser capaz de usar o formato de ambos os sistemas. Como a maioria dos gateways não está ciente dos formatos de identificador de entrada, a conversão de identificadores de entrada é rara.
  
Outra propriedade mapeável que não deve ser traduzida com frequência é o nome de exibição. Os gateways devem armazenar nomes de exibição e transmiti-los, mas não necessariamente traduzi-los. 
  

