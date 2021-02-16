---
title: Tipos de provedores de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406161"
---
# <a name="types-of-transport-providers"></a>Tipos de provedores de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todos os provedores de transporte suportam uma variedade de recursos padrão, como:
  
- Fornecendo segurança adequada para o sistema de mensagens subjacente.
    
- Enviar e receber mensagens do sistema de mensagens subjacente.
    
- Expor os tipos de endereço aos quais os provedores de transporte suportam para que o spooler MAPI e os aplicativos cliente possam usá-los adequadamente.
    
- Aceitar entrega para destinatários específicos.
    
Além disso, o MAPI oferece suporte a dois tipos especializados de provedores para sistemas de mensagens específicos.
  
|**Tipo de transporte**|**Funcionalidade adicionada**|
|:-----|:-----|
|Transporte Remoto  <br/> |Habilita a interoperabilidade com clientes conectados remotamente.  <br/> |
|Transporte TNEF  <br/> |Permite que as propriedades MAPI sejam preservadas em sistemas de mensagens que não as suportam.  <br/> |
   
Os transporte TNEF são usados para traduzir mensagens entre sistemas de mensagens que suportam diferentes conjuntos de propriedades MAPI. Os transporte TNEF usam a interface [MAPI ITnef : IUnknown](itnefiunknown.md) para converter quaisquer propriedades que o sistema de destino não possa representar diretamente em um fluxo de dados binário que possa ser anexado à mensagem. Posteriormente, outro transporte TNEF pode usar **ITnef** para decodificar o fluxo de dados e disponibilizar as propriedades MAPI originais para aplicativos cliente. Além disso, o suporte a TNEF será necessário se o transporte precisar dar suporte a classes de mensagens personalizadas. Para obter informações sobre a implementação de transporte TNEF, consulte [Desenvolvendo um provedor TNEF-Enabled transporte de transporte.](developing-a-tnef-enabled-transport-provider.md)
  
Se seu provedor de transporte não for um desses tipos, você terá que implementá-lo com as funções MAPI básicas e as funções de rede disponíveis em sua plataforma de destino.
  

