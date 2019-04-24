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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315376"
---
# <a name="types-of-transport-providers"></a>Tipos de provedores de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todos os provedores de transporte dão suporte a uma variedade de recursos padrão, como:
  
- Fornecer segurança adequada para o sistema de mensagens subjacente.
    
- Envio e recebimento de mensagens do sistema de mensagens subjacente.
    
- Expondo os tipos de endereço que os provedores de transporte dão suporte para que o spooler MAPI e os aplicativos cliente possam usá-los adequadamente.
    
- Aceitar a entrega para destinatários específicos.
    
Além disso, o MAPI dá suporte a dois tipos especializados de provedores para sistemas de mensagens específicos.
  
|**Tipo de transporte**|**Funcionalidade adicionada**|
|:-----|:-----|
|Transporte remoto  <br/> |Permite a interoperabilidade com clientes conectados remotamente.  <br/> |
|Transporte TNEF  <br/> |Permite que as propriedades MAPI sejam preservadas em sistemas de mensagens que não dão suporte a eles.  <br/> |
   
Os transportes TNEF são usados para converter mensagens entre sistemas de mensagens que oferecem suporte a diferentes conjuntos de propriedades MAPI. Transportes TNEF use a interface MAPI [ITnef: IUnknown](itnefiunknown.md) para converter qualquer propriedade que o sistema de destino não possa representar diretamente para um fluxo de dados binários que possa ser anexado à mensagem. Mais tarde, outro transporte TNEF pode usar o **ITnef** para decodificar o fluxo de dados e tornar as propriedades MAPI originais disponíveis para aplicativos cliente. Além disso, o suporte a TNEF será necessário se o transporte precisar oferecer suporte a classes de mensagens personalizadas. Para obter informações sobre a implementação de transportes TNEF, consulte [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
  
Se o seu provedor de transporte não for um desses tipos, você terá que implementá-lo com as funções básicas de MAPI e de rede disponíveis na sua plataforma de destino.
  

