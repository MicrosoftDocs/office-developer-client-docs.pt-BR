---
title: Registro de uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ccc2758b59a9227afbc50360102e793892bbdc52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328403"
---
# <a name="registering-for-a-notification"></a>Registro de uma notificação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode se registrar no catálogo de endereços ou notificações do repositório de mensagens como parte do processo de inicialização.
  
O MAPI dá suporte à notificação no catálogo de endereços independentemente de qualquer um dos provedores de catálogo de endereços oferecer suporte a ele. O suporte para notificação em repositórios de mensagens depende de um determinado provedor de armazenamento de mensagens. Para determinar se um determinado provedor de repositório de mensagens oferece suporte a notificações, verifique sua propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Se o repositório de mensagens suportar notificações, o bit STORE_NOTIFY_OK será definido. 
  
Registre-se para notificações chamando o método **Advise** de um objeto de origem de aviso. Muitos objetos implementam o **aviso** e os clientes podem se registrar nesses objetos de várias maneiras. 
  
 **Para registrar uma notificação**
  
1. Crie um objeto de coletor de aviso MAPI e aumente sua contagem de referência.
    
2. Se apropriado, chame [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para criar um objeto de coletor de aviso que envolve o coletor de aviso original e, em seguida, libere o coletor de aviso original.. 
    
3. Chame um dos seguintes métodos de **aviso** para concluir o registro: 
    
  - Chamar [IMAPISession:: avisar](imapisession-advise.md) para registrar notificações de sessão ou para notificações em um catálogo de endereços ou objeto de repositório de mensagens. 
    
  - Chamar [IAddrBook:: avisar](iaddrbook-advise.md) para registrar notificações do catálogo de endereços ou para notificações em um usuário de mensagens, um contêiner ou uma lista de distribuição. 
    
  - Chamar [IABLogon:: avisar](iablogon-advise.md) para registrar-se diretamente com um provedor de catálogo de endereços para notificações em um usuário de mensagens, um contêiner ou uma lista de distribuição. 
    
  - Chamar [IMsgStore:: avisar](imsgstore-advise.md) para registrar notificações de repositório de mensagens ou para notificações em uma pasta ou uma mensagem. 
    
  - Chamar [IMSLogon:: avisar](imslogon-advise.md) para registrar-se diretamente com um provedor de repositório de mensagens para notificações em uma pasta ou uma mensagem. 
    
  - Call [IMAPITable:: Advise](imapitable-advise.md) para registrar-se para notificações de tabela. 
    
4. Armazenar em cache o número de conexão retornado de **Advise**.
    
5. Se estiver usando um coletor de aviso de quebra, solte-o. Quando o coletor de aviso de quebra for registrado, você não precisa mais dele.
    
Chamar * * IMAPISession:: Advise * * permite que você se registre para notificações de erro crítico na sessão geral ou para várias notificações em objetos individuais. As sessões enviam notificações de erro críticas aos clientes conectados a sessões compartilhadas quando outro cliente usando a sessão compartilhada chama o método [IMAPISession:: logoff](imapisession-logoff.md) . Para registrar-se para notificações de sessão, passe NULL para o parâmetro de identificador de entrada. Para registrar-se para notificações em um objeto individual, passe o identificador de entrada do objeto. O método **IMAPISession** encaminha a chamada para o provedor de serviços apropriado, conforme determinado pela parte **MAPIUID** do identificador de entrada. Chamar **IMAPISession:: Advise** para registrar para notificações de objeto é mais simples do que chamar o método **Advise** de um provedor de serviços. 
  
O registro no catálogo de endereços é semelhante ao registro na sessão. Para registrar a notificação de erro crítico no catálogo de endereços, passe NULL para o identificador de entrada. Para registrar notificações em um objeto de catálogo de endereços específico, especifique o identificador de entrada apropriado e evento ou eventos de interesse. Lembre-se de que muitos provedores de catálogo de endereços não dão suporte a notificações em objetos individuais. Em vez disso, eles dão suporte a notificações de tabela em suas tabelas de conteúdo e hierarquia. 
  
É uma boa prática lançar o coletor de aviso que você implementa ou cria com o [HrAllocAdviseSink](hrallocadvisesink.md) imediatamente após um retorno bem-sucedido de uma chamada de **aviso** . Isso ocorre porque é possível que os provedores de serviços liberem o seu coletor de aviso após a chamada de **aviso** , mas antes de uma chamada a **Unadvise** ser feita. Depois de receber a fonte de aviso de um ponteiro para seu coletor de avisos e a contagem de referência tiver sido incrementada nesse coletor de aviso, é prudente liberá-lo, a menos que você tenha um uso de longo prazo para ele. 
  
> [!NOTE]
> Todos os números de conexão que representam registros de consultoria válidos não serão liberados até que a chamada de **Unadvise** seja feita. 
  

