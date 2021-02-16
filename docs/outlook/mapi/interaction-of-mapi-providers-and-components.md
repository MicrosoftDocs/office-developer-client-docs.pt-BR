---
title: Interação de provedores e componentes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434659"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interação de provedores e componentes MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de serviços MAPI de qualquer tipo devem seguir determinadas diretrizes para trabalhar com outros componentes MAPI. Cada provedor de serviços deve:
  
- Use o provedor e os objetos de logon adequados para inicialização.
    
- Retornar uma tabela de expedição de pontos de entrada do provedor para o sistema de mensagens após a inicialização.
    
- Registre uma linha de tabela de status MAPI para cada recurso pertencente ao provedor e chame o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) nos horários apropriados. 
    
- Use o [método IMAPISupport::NewUID](imapisupport-newuid.md) para obter UIDs (identificadores exclusivos) válidos. 
    
- Suporte às interfaces MAPI comuns nos objetos que ele retorna.
    
- Use as funções de alocação de memória MAPI para alocar memória retornada para aplicativos cliente e liberar memória alocada por outras partes do subsistema MAPI.
    
- Mantenha uma seção de perfil, se necessário, para armazenar credenciais no sistema de mensagens subjacente.
    
- Use o [método IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar quaisquer funções de pré-processamento de mensagens. 
    
- Inclua os arquivos de header adequados (incluindo mapispi.h) que definem constantes, estruturas, interfaces e valores de retorno comuns.
    
- Siga as convenções de formato de endereço para tipos de endereços comuns.
    

