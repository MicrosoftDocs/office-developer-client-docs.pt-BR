---
title: Registrando-se para uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ccc2758b59a9227afbc50360102e793892bbdc52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424900"
---
# <a name="registering-for-a-notification"></a>Registrando-se para uma notificação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode se registrar para o livro de endereços ou notificações do armazenamento de mensagens como parte de seu processo de inicialização.
  
MAPI supports notification on the address book regardless of whether any of the address book providers support it. O suporte para notificação em armazenamentos de mensagens depende do provedor de armazenamento de mensagens específico. Para determinar se um determinado provedor de repositório de mensagens oferece suporte a notificações, verifique sua **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) . Se o armazenamento de mensagens suportar notificações, o STORE_NOTIFY_OK bit será definido. 
  
Registre-se para notificações chamando o método Advise de um objeto **de** origem de aviso. Muitos objetos **implementam o Advise** e os clientes podem se registrar com esses objetos de várias maneiras. 
  
 **Para registrar-se para uma notificação**
  
1. Crie um objeto sink de alerta MAPI e incremente sua contagem de referência.
    
2. Se apropriado, chame [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para criar um objeto de pia de aviso que envolve seu pia de aviso original e, em seguida, libere o pia de conselhos original. 
    
3. Chame um dos seguintes métodos **Advise** para concluir o registro: 
    
  - Chame [IMAPISession::Advise](imapisession-advise.md) para registrar-se para notificações de sessão ou para notificações em um objeto de armazenamento de mensagens ou de um livro de endereços. 
    
  - Chame [IAddrBook::Advise](iaddrbook-advise.md) para registrar-se para notificações do livro de endereços ou para notificações em um usuário de mensagens, contêiner ou lista de distribuição. 
    
  - Chame [IABLogon::Advise](iablogon-advise.md) para registrar-se diretamente com um provedor de agendamento de endereços para notificações em um usuário de mensagens, contêiner ou lista de distribuição. 
    
  - Chame [IMsgStore::Advise](imsgstore-advise.md) para registrar-se para notificações do repositório de mensagens ou para notificações em uma pasta ou mensagem. 
    
  - Chame [IMSLogon::Advise](imslogon-advise.md) para registrar-se diretamente com um provedor de armazenamento de mensagens para notificações em uma pasta ou mensagem. 
    
  - Chame [IMAPITable::Advise](imapitable-advise.md) para se registrar para notificações de tabela. 
    
4. Armazenar em cache o número de conexão retornado de **Advise**.
    
5. Se estiver usando um sink de aconselhá-lo, solte-o. Depois que o aconselhado empacotado é registrado, você não precisa mais dele.
    
Chamar ** IMAPISession::Advise ** permite que você se registre para notificações de erro crítico na sessão geral ou para várias notificações em objetos individuais. As sessões enviam notificações de erro críticas aos clientes conectados a sessões compartilhadas quando outro cliente que usa a sessão compartilhada chama o método [IMAPISession::Logoff.](imapisession-logoff.md) Para se registrar para notificações de sessão, passe NULL para o parâmetro identificador de entrada. Para registrar notificações em um objeto individual, passe o identificador de entrada do objeto. O **método IMAPISession** encaminha a chamada para o provedor de serviços apropriado, conforme determinado pela parte **MAPIUID** do identificador de entrada. Chamar **IMAPISession::Advise** para registrar para notificações de objeto é mais simples do que chamar o método Advise de um provedor **de** serviços. 
  
Registrar-se com o livro de endereços é semelhante ao registro na sessão. Para se registrar para notificação de erro crítico do livro de endereços, passe NULL para o identificador de entrada. Para se registrar para notificações em um objeto de agendamento específico, especifique o identificador de entrada apropriado e o evento ou eventos de interesse. Esteja ciente de que muitos provedores de agendas de endereços não suportam notificações em objetos individuais. Em vez disso, eles suportam notificações de tabela em seus conteúdos e tabelas de hierarquia. 
  
É uma boa prática liberar o sink de aconselhância que você implementa ou cria com [HrAllocAdviseSink](hrallocadvisesink.md) imediatamente após um retorno bem-sucedido de uma **chamada Desconselhá-lo.** Isso porque é possível que os provedores de serviços liberem seu cliente de consultoria após **a** chamada Desconselhá-lo, mas antes de uma chamada Não Prevista ser feita.  Depois de dar à fonte de conselhos um ponteiro para o seu sink de consultoria e a contagem de referência tiver sido incrementada nesse sink de conselhos, é sensato liberá-lo, a menos que você tenha um uso de longo prazo para ele. 
  
> [!NOTE]
> Todos os números de conexão que representam registros de consultoria válidos não serão lançados até que a chamada **NãoVise** seja feita. 
  

