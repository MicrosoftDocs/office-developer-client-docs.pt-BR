---
title: Implementando uma função de ponto de entrada do provedor de agendamento de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409710"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementando uma função de ponto de entrada do provedor de agendamento de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um aplicativo cliente chama [MAPILogonEx](mapilogonex.md) para iniciar uma sessão usando um perfil que contém seu provedor de agendamento de endereços, o MAPI carrega seu provedor e todos os outros que fazem parte do perfil. MAPI learns of the name of your provider's entry point function by looking in the profile. Lembre-se de que essa função não é a mesma que uma função de ponto de entrada de DLL; consulte a documentação **de DllMain** na documentação do Win32. 
  
Há várias entradas, algumas das quais devem aparecer no arquivo de configuração mapisvc.inf, incluídas na seção de perfil de cada provedor de agendas de endereços. A tabela a seguir lista essas entradas de seção de perfil e se o arquivo mapisvc.inf deve ou não incluí-las.
  
|**Entrada de seção de perfil**|**requisito mapisvc.inf**|
|:-----|:-----|
|PR_DISPLAY_NAME= cadeia de _caracteres_ <br/> |Opcional  <br/> |
|PR_PROVIDER_DISPLAY= cadeia de _caracteres_ <br/> |Obrigatório  <br/> |
|PR_PROVIDER_DLL_NAME= _nome de arquivo DLL_ <br/> |Obrigatório  <br/> |
|PR_RESOURCE_TYPE= _long_ <br/> |Obrigatório  <br/> |
|PR_RESOURCE_FLAGS= _bitmask_ <br/> |Opcional  <br/> |
   
Seu provedor de agendamento de endereços pode colocar essas informações em um perfil diretamente chamando o método [IMAPIProp::SetProps](imapiprop-setprops.md) da seção de perfil ou indiretamente modificando MAPISVC.INF. Os perfis são criados usando as informações relevantes no MAPISVC. INF para os provedores de serviços ou serviços de mensagem selecionados. Para obter mais informações sobre a organização e o conteúdo do MAPISVC. INF, consulte [Formato de arquivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).
  
O nome da função de ponto de entrada DLL do seu provedor de endereços deve ser [ABProviderInit](abproviderinit.md) e deve estar em conformidade com o protótipo **ABProviderInit.** Execute as seguintes tarefas na função de ponto de entrada DLL do provedor: 
  
- Verifique a versão da interface do provedor de serviços (SPI) para verificar se o MAPI está usando uma versão compatível com a versão que seu provedor de agendas está usando.
    
- In instantiate an address book provider object.
    
Não chame **MAPIInitialize** ou **MAPIUninitialize** nesta função. 
  
A função de ponto de entrada de DLL insta em um objeto de provedor e retorna a MAPI um ponteiro para esse objeto. 
  

