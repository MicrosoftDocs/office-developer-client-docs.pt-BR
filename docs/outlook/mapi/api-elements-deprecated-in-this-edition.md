---
title: Elementos de API preterido nesta edição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436885"
---
# <a name="api-elements-deprecated-in-this-edition"></a>Elementos de API preterido nesta edição

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os seguintes elementos da API foram preterido no Microsoft Outlook 2013. Eles não são mais suportados e você não deve usá-los em novos projetos.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Preterição de opções de mensagem e destinatário

Os seguintes elementos da API foram preterido nesta versão devido a opções obsoletas de mensagem e destinatário:
  
- **IXPLogon::RegisterOptions**— O subsistema MAPI não chama mais esse método para estabelecer valores padrão para opções de mensagem e destinatário para um provedor de transporte.
    
- **OPTIONDATA**— Essa estrutura de dados que suportava propriedades para opções de mensagem e destinatário está obsoleta. O subsistema mapi não chama **mais IXPLogon::RegisterOptions** para obter qualquer mensagem ou opções de destinatário que um provedor de transporte suporta para um tipo de endereço específico. 
    
- **OPTIONCALLBACK**— Este protótipo de função, que um provedor de transporte usou para declarar uma função de retorno de chamada e que, por sua vez, o subsistema MAPI usado para resolver as propriedades do provedor, é obsoleto. O subsistema mapi não chama **mais IXPLogon::RegisterOptions** ou usa qualquer função de retorno de chamada retornada pelo provedor de transporte. 
    
- **IMAPISession::MessageOptions**— os provedores de serviço e cliente MAPI não devem mais chamar esse método para exibir propriedades ou permitir que os usuários deverão definir propriedades que controlam uma mensagem e um tipo de endereço específicos. O método sempre retorna MAPI_E_NOT_FOUND, o que indica que não há opções de mensagem para a mensagem específica.
    
- **IMAPISession::QueryDefaultMessageOpt**— os provedores de serviço e cliente MAPI não devem mais chamar esse método para recuperar propriedades que controlam as opções de mensagem para um tipo de endereço específico. O método não retorna mais um ponteiro para qualquer matriz de valores de propriedade.
    
- **IAddrBook::RecipOptions**— os provedores de serviço e cliente MAPI não devem mais chamar esse método para exibir propriedades ou permitir que os usuários deverão definir propriedades que controlam o processamento para um destinatário de um tipo de endereço específico. O método sempre retorna MAPI_W_ERRORS_RETURNED, o que indica que não há opções de destinatário para o destinatário específico.
    
- **IAddrBook::QueryDefaultRecipOpt**— os provedores de serviço e cliente MAPI não devem mais chamar esse método para recuperar propriedades que controlam as opções de destinatário para um tipo de endereço específico. O método não retorna mais um ponteiro para qualquer matriz de valores de propriedade.
    
## <a name="see-also"></a>Confira também



[Introdução à Referência de MAPI do Outlook](getting-started-with-the-outlook-mapi-reference.md)

