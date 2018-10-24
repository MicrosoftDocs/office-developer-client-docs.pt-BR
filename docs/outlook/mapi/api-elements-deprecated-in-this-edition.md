---
title: Elementos de API preteridos nesta edição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Última modificação: 25 de julho de 2012'
ms.openlocfilehash: e40bcbfffc6f149837f4a11351f2bdbbf0dcc524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571595"
---
# <a name="api-elements-deprecated-in-this-edition"></a>Elementos de API preteridos nesta edição

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os seguintes elementos de API são reduzidos no Microsoft Outlook 2013. Eles não são mais suportados e você não deve usá-los em novos projetos.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Preterir da mensagem e destinatários opções

Os seguintes elementos de API são preteridos nesta versão devido a mensagem obsoleta e opções de destinatário:
  
- **IXPLogon::RegisterOptions**— subsistema de MAPI não são mais chama esse método para estabelecer a todos os valores padrão para as opções de mensagem e destinatário para um provedor de transporte.
    
- **OPTIONDATA**— essa estrutura de dados que suporte a propriedades para as opções de mensagem e destinatário é obsoleta. O subsistema de MAPI não são mais chama **IXPLogon::RegisterOptions** para obter qualquer mensagem ou opções de destinatário que oferece suporte a um provedor de transporte para um tipo de endereço específica. 
    
- **OPTIONCALLBACK**— esse protótipo de função para um provedor de transporte usado para declarar uma função de retorno de chamada e que, por sua vez, o subsistema MAPI usado para resolver as propriedades do provedor, é obsoleto. Não há mais o subsistema MAPI chama **IXPLogon::RegisterOptions** ou usa qualquer função de retorno de chamada retornada pelo provedor de transporte. 
    
- **IMAPISession::MessageOptions**— provedores MAPI de cliente e o serviço não são mais devem chamar esse método para exibir as propriedades ou permitir que os usuários definir propriedades que controlam um determinado tipo de mensagem e o endereço. O método sempre retornará E_NOT_FOUND, que indica que não há nenhuma opção de mensagem para a mensagem específica.
    
- **IMAPISession::QueryDefaultMessageOpt**— provedores MAPI de cliente e o serviço não são mais devem chamar esse método para recuperar as propriedades que controlam as opções de mensagem para um tipo de endereço específica. O método não retorna um ponteiro para qualquer conjunto de valores de propriedade.
    
- **IAddrBook::RecipOptions**— provedores MAPI de cliente e o serviço não são mais devem chamar esse método para exibir as propriedades ou permitir que os usuários definir propriedades que o processamento de controle para um destinatário de um tipo de endereço específica. O método sempre retornará MAPI_W_ERRORS_RETURNED, que indica que não existem opções destinatários para o destinatário específico.
    
- **IAddrBook::QueryDefaultRecipOpt**— provedores MAPI de cliente e o serviço não são mais devem chamar esse método para recuperar as propriedades que controlam as opções de destinatário para um tipo de endereço específica. O método não retorna um ponteiro para qualquer conjunto de valores de propriedade.
    
## <a name="see-also"></a>Confira também



[Introdução à Referência de MAPI do Outlook](getting-started-with-the-outlook-mapi-reference.md)

