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
ms.openlocfilehash: 91c1d9293108b96fde43b769c97ec673f82a8cb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563027"
---
# <a name="gateway-mapping-responsibilities"></a>Responsabilidades de mapeamento do gateway

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um gateway de reconhecimento de MAPI recebe uma mensagem contendo propriedades nomeadas em um dos conjuntos de propriedade especial é designados para conter as propriedades podem ser mapeados gateway, o gateway deve mapear todas as propriedades para o protocolo do destino do sistema de mensagens. Embora o MAPI recomenda que gateways manipular nomeadas todas as propriedades nos conjuntos de propriedade especial, gateways esperados para lidar com apenas dois: endereço e o tipo de endereço de email. Como as propriedades de tipo de endereço e o endereço de email diretamente afetam a transmissão de mensagens, é fundamental que os gateways suportam o mapeamento dessas duas propriedades. Porque as chaves de pesquisa consistem em tipo de endereço e o endereço de um usuário, eles também devem ser traduzidos se possível.
  
Identificadores de entrada não deverão ser manipulados com frequência. Para habilitar o mapeamento de um identificador de entrada que se origina de um sistema de mensagens a um identificador de entrada que pode ser usado por outro sistema de mensagens, o gateway deve ser capaz de usar o formato dos dois sistemas. Porque a maioria dos gateways não estão cientes dos formatos de identificador de entrada, a tradução dos identificadores de entrada é rara.
  
Outra propriedade podem ser mapeada que não é esperada a serem convertidos frequentemente é o nome de exibição. Gateways devem armazenar nomes para exibição e transmiti-las, mas não necessariamente traduzi-los. 
  

