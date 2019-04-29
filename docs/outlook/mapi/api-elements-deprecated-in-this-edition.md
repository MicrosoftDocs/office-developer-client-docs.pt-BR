---
title: Elementos de API preTeridos nesta edição
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
# <a name="api-elements-deprecated-in-this-edition"></a>Elementos de API preTeridos nesta edição

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os seguintes elementos da API são preteridos no Microsoft Outlook 2013. Eles não são mais suportados e você não deve usá-los em novos projetos.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Substituição de opções de mensagens e destinatários

Os seguintes elementos de API são preteridos nesta versão devido às opções obsoletas de mensagem e destinatário:
  
- **IXPLogon:: registeroptions**, o subsistema MAPI não chama mais este método para estabelecer qualquer valor padrão para as opções de mensagem e destinatário de um provedor de transporte.
    
- **OPTIONDATA**— essa estrutura de dados que dá suporte a propriedades de mensagens e opções de destinatário é obsoleta. O subsistema MAPI não chama mais **IXPLogon:: registeroptions** para obter qualquer opção de mensagens ou destinatários que um provedor de transporte ofereça suporte a um determinado tipo de endereço. 
    
- **OPTIONCALLBACK**— este protótipo de função, que é um provedor de transporte usado para declarar uma função de retorno de chamada e que, por sua vez, o subsistema MAPI usado para resolver as propriedades do provedor, é obsoleto. O subsistema MAPI não chama mais **IXPLogon:: registeroptions** ou usa qualquer função de retorno de chamada retornada pelo provedor de transporte. 
    
- **IMAPISession:: messageoptions**— o cliente MAPI e os provedores de serviço não devem mais chamar este método para exibir propriedades ou permitir que os usuários definam propriedades que controlam um determinado tipo de mensagem e endereço. O método sempre retorna MAPI_E_NOT_FOUND, que indica que não há opções de mensagem para a mensagem específica.
    
- **IMAPISession:: QueryDefaultMessageOpt**— o cliente MAPI e os provedores de serviço não devem mais chamar esse método para recuperar propriedades que controlam as opções de mensagem para um tipo de endereço específico. O método não retorna mais um ponteiro para qualquer matriz de valores de propriedade.
    
- **IAddrBook:: RecipOptions**— o cliente MAPI e os provedores de serviço não devem mais chamar esse método para exibir propriedades ou permitir que os usuários definam propriedades que controlam o processamento de um destinatário de um determinado tipo de endereço. O método sempre retorna MAPI_W_ERRORS_RETURNED, que indica que não há opções de destinatário para o destinatário específico.
    
- **IAddrBook:: QueryDefaultRecipOpt**— o cliente MAPI e os provedores de serviço não devem mais chamar esse método para recuperar propriedades que controlam as opções de destinatário para um determinado tipo de endereço. O método não retorna mais um ponteiro para qualquer matriz de valores de propriedade.
    
## <a name="see-also"></a>Confira também



[Introdução à Referência de MAPI do Outlook](getting-started-with-the-outlook-mapi-reference.md)

