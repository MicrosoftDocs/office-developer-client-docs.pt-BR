---
title: Implementar uma função de ponto de entrada do provedor de catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332799"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementar uma função de ponto de entrada do provedor de catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um aplicativo cliente chama o [funçãomapilogonex](mapilogonex.md) para iniciar uma sessão usando um perfil que contém seu provedor de catálogo de endereços, o MAPI carrega seu provedor e todos os outros que fazem parte do perfil. O MAPI aprende o nome da função de ponto de entrada do provedor procurando no perfil. Lembre-se de que essa função não é o mesmo que uma função de ponto de entrada DLL; consulte a documentação do **DllMain** na documentação do Win32. 
  
Há várias entradas, algumas das quais devem aparecer no arquivo de configuração MAPISVC. inf, incluídas na seção de perfil de cada provedor de catálogo de endereços. A tabela a seguir lista essas entradas de seção de perfil e se o arquivo MAPISVC. inf deve ou não ser incluído.
  
|**Entrada da seção de perfil**|**requisitos de MAPISVC. inf**|
|:-----|:-----|
|PR_DISPLAY_NAME = _cadeia de caracteres_ <br/> |Opcional  <br/> |
|PR_PROVIDER_DISPLAY = _cadeia de caracteres_ <br/> |Obrigatório  <br/> |
|PR_PROVIDER_DLL_NAME = _dll filename_ <br/> |Obrigatório  <br/> |
|PR_RESOURCE_TYPE = _Long_ <br/> |Obrigatório  <br/> |
|PR_RESOURCE_FLAGS = _bitmask_ <br/> |Opcional  <br/> |
   
Seu provedor de catálogo de endereços pode colocar essas informações em um perfil diretamente chamando o método [IMAPIProp::](imapiprop-setprops.md) SetProps da seção de perfil, ou indiretamente, modificando MAPISVC. inf. Os perfis são criados usando as informações relevantes em MAPISVC. INF para os provedores de serviço ou serviços de mensagem selecionados. Para obter mais informações sobre a organização e o conteúdo de MAPISVC. INF, consulte [formato de arquivo de MapiSvc. inf](file-format-of-mapisvc-inf.md).
  
O nome da função de ponto de entrada DLL do provedor do catálogo de endereços deve ser [ABProviderInit](abproviderinit.md) e deve estar em conformidade com o protótipo do **ABProviderInit** . Execute as seguintes tarefas na função de ponto de entrada DLL do provedor: 
  
- Verifique a versão da interface do provedor de serviços (SPI) para verificar se o MAPI está usando uma versão compatível com a versão que seu provedor de catálogo de endereços está usando.
    
- Crie uma instância de um objeto de provedor de catálogo de endereços.
    
Não chame **MAPIInitialize** ou **MAPIUninitialize** nesta função. 
  
A função de ponto de entrada de DLL instancia um objeto Provider e retorna para um ponteiro MAPI a esse objeto. 
  

