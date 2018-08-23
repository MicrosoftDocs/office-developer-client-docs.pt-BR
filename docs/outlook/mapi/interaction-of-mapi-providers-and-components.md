---
title: Interação de provedores e componentes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c81da7673d6c0c59de6992bc46362069daf71b42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592623"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interação de provedores e componentes MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de serviço MAPI de qualquer tipo devem seguir determinadas diretrizes para trabalhar com outros componentes MAPI. Cada provedor de serviços deve:
  
- Use os objetos de logon e o provedor adequados para inicialização.
    
- Retorne uma tabela de expedição de pontos de entrada do provedor para o sistema de mensagens na inicialização.
    
- Registrar uma linha de tabela de status MAPI para cada recurso pertencente ao provedor e chamar o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) em momentos apropriados. 
    
- Use o método [IMAPISupport::NewUID](imapisupport-newuid.md) para obter identificadores exclusivos válidos (UIDs). 
    
- Suporte para as interfaces MAPI comuns em objetos que ela retorna.
    
- Use as funções de alocação de memória MAPI para alocar memória retornada para aplicativos cliente e para liberar memória alocada por outras partes do subsistema de MAPI.
    
- Manter uma seção de perfil, se necessário, para armazenar credenciais para o sistema de mensagens subjacente.
    
- Use o método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar qualquer mensagem de pré-processamento funções. 
    
- Inclua os arquivos de cabeçalho adequadas (incluindo mapispi.h) que definem as constantes comuns, estruturas, interfaces e valores de retorno.
    
- Siga as convenções de formato de endereço para tipos de endereço comuns.
    

