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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332169"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interação de provedores e componentes MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de serviço MAPI de qualquer tipo devem seguir algumas diretrizes para trabalhar com outros componentes MAPI. Cada provedor de serviços deve:
  
- Use o provedor e os objetos de logon adequados para inicialização.
    
- Retornar uma tabela de expedição de pontos de entrada de provedor para o sistema de mensagens na inicialização.
    
- Registre uma linha de tabela de status MAPI para cada recurso pertencente ao provedor e chame o método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) em momentos apropriados. 
    
- Use o método [IMAPISupport:: NewUID](imapisupport-newuid.md) para obter UIDs (identificadores exclusivos) válidos. 
    
- Suportar as interfaces comuns de MAPI em objetos que ele retorna.
    
- Use as funções de alocação de memória MAPI para alocar memória retornada aos aplicativos cliente e para liberar a memória alocada por outras partes do subsistema MAPI.
    
- Mantenha uma seção de perfil, se necessário, para armazenar credenciais para o sistema de mensagens subjacente.
    
- Use o método [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar qualquer função de pré-processamento de mensagem. 
    
- Inclua os arquivos de cabeçalho adequados (incluindo mapispi. h) que definem constantes, estruturas, interfaces e valores de retorno comuns.
    
- Siga as convenções de formato de endereço para tipos de endereço comuns.
    

