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
ms.openlocfilehash: b60a80bc0ede0c2800f6cfd98a98f498b93a1d8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767416"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementar uma função de ponto de entrada do provedor de catálogo de endereços

  
  
**Aplica-se a**: Outlook 
  
Quando a chamadas do aplicativo de cliente [MAPILogonEx](mapilogonex.md) para iniciar uma sessão usando um perfil que contém seu provedor de catálogo de endereços, MAPI carrega seu provedor e todas as outras pessoas que fazem parte do perfil. MAPI aprende do nome da função do ponto de entrada do seu provedor observando o perfil. Lembre-se de que essa função não é o mesmo que uma função de ponto de entrada DLL; Consulte a documentação para **DllMain** na documentação do Win32. 
  
Existem várias entradas, alguns dos quais devem ser exibida no arquivo de configuração Mapisvc, que estão incluídas na seção de perfil de cada provedor de catálogo de endereços. A tabela a seguir lista essas entradas da seção de perfil e o arquivo Mapisvc ou não deve inclui-los.
  
|**Entrada de seção de perfil**|**requisito de Mapisvc**|
|:-----|:-----|
|PR_DISPLAY_NAME = _cadeia de caracteres_ <br/> |Opcional  <br/> |
|PR_PROVIDER_DISPLAY = _string_ <br/> |Obrigatório  <br/> |
|PR_PROVIDER_DLL_NAME = o _nome do arquivo DLL_ <br/> |Obrigatório  <br/> |
|PR_RESOURCE_TYPE = _longo_ <br/> |Obrigatório  <br/> |
|PR_RESOURCE_FLAGS = _bitmask_ <br/> |Opcional  <br/> |
   
Seu provedor de catálogo de endereços pode fazer essas informações em um perfil diretamente chamando o método de [IMAPIProp::SetProps](imapiprop-setprops.md) da seção do seu perfil ou indiretamente modificando Mapisvc. Perfis são criados usando as informações relevantes na MAPISVC. INF para os provedores de serviço selecionado ou os serviços de mensagem. Para obter mais informações sobre a organização e o conteúdo de MAPISVC. INF, consulte o [Formato de arquivo do Mapisvc](file-format-of-mapisvc-inf.md).
  
O nome da função de ponto de entrada DLL do seu provedor catálogo de endereços deve ser [ABProviderInit](abproviderinit.md) e ele deve se adequar ao protótipo **ABProviderInit** . Execute as seguintes tarefas na função de ponto de entrada DLL do seu provedor: 
  
- Verifica a versão da interface do provedor de serviço (SPI) para certificar-se de que MAPI está usando uma versão compatível com a versão que está usando o seu provedor de catálogo de endereços.
    
- Criar uma instância de um objeto de provedor de catálogo de endereços.
    
Não chame **MAPIInitialize** ou **MAPIUninitialize** nessa função. 
  
A função do ponto de entrada DLL instancia um objeto de provedor e retorna ao MAPI um ponteiro para aquele objeto. 
  

