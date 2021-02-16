---
title: Sessões MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c5a7c137-393e-40ff-a2b9-afe02da2435a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3dd55d8ee3cb2751fb27184f0069ae831e2164ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435870"
---
# <a name="mapi-sessions"></a>Sessões MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para que o aplicativo cliente possa chamar um sistema de mensagens subjacente, ele deve estabelecer uma sessão, ou conexão, com o subsistema MAPI.
  
As sessões são iniciadas quando um usuário faz o login, um processo que acessa um perfil válido e valida o sistema de mensagens e as credenciais do serviço de mensagens. Em seguida, o processo garante que todos os serviços de mensagens do perfil sejam configurados corretamente. A interface do cliente usada determina a chamada de logon. Clientes MAPI chamam a [função MAPILogonEx.](mapilogonex.md) 
  
A configuração do serviço de mensagens é uma das partes mais importantes do processo de logon. O perfil é a fonte inicial para informações de configuração. Se a informação de um determinado serviço de mensagens estiver ausente, o processo de logon tentará solicitar que o usuário o fornegue. Isso nem sempre é bem-sucedido por dois motivos: primeiro, solicitar ao usuário a exibição de uma caixa de diálogo. É possível que os clientes não permitem a exibição de uma interface do usuário passando um sinalizador para a chamada de logon. Segundo, o usuário poderia cancelar a caixa de diálogo antes que as informações necessárias pudessem ser adicionadas.
  
Quando um processo de logon falha uma vez, o usuário é informado da falha e tem a chance de tentar novamente ou corrigir a condição de erro. Mais uma vez, uma interface do usuário será exibida, se o cliente permitir e o usuário será solicitado a inserir os dados que estão faltando. Se esta segunda tentativa não for bem-sucedida, o MAPI desabilitará todos os provedores de serviços no serviço de mensagens durante a sessão. Na verdade, todo o serviço de mensagens está desabilitado. Isso significa que nenhum dos provedores de serviços no serviço de mensagens pode funcionar. Isso é feito porque, se um provedor falhar no logon, os outros provedores geralmente também falharão. O processo de logon pode falhar devido a um caminho inválido para um recurso necessário, uma versão incompatível de MAPI, um servidor de mensagens indisponível ou corrupção de dados. 
  
Os clientes podem especificar um dos dois tipos de sessões a serem estabelecidas na chamada de logon: uma sessão individual ou uma sessão compartilhada. Sessões individuais são conexões privadas; há uma relação um-para-um entre um aplicativo cliente e a sessão que ele está usando. Como consequência, os aplicativos cliente que compartilham uma sessão também compartilham um perfil. As sessões compartilhadas são estabelecidas uma vez, mas podem ser usadas por outros aplicativos cliente que precisem usá-las. O perfil e as credenciais são especificados apenas com o logon inicial. 
  
Os clientes podem fazer logoff várias vezes como o mesmo usuário ou como vários usuários. O MAPI não impede isso. Alguns provedores de serviços, no entanto, podem não ser tão flexíveis, retornando o valor de erro MAPI_E_SESSION_LIMIT nas tentativas de logon subsequentes. Provedores de serviços com limitações de hardware subjacentes podem ser necessários para impor um limite de sessão.
  
A função chama para estabelecer uma sessão tem uma coleção de sinalizadores e parâmetros que controlam como a sessão é criada. O cliente especifica um nome de perfil opcional e uma alça de janela que age como a janela pai de todas as caixas de diálogo exibidas. Os sinalizadores incluem MAPI_NEW_SESSION, que solicita que uma nova sessão individual (em vez de uma sessão compartilhada) seja estabelecida e o sinalizador MAPI_LOGON_UI interface do usuário. O sinalizador da interface do usuário é definido para solicitar uma caixa de diálogo de logon.
  
A ilustração a seguir mostra como esses diversos parâmetros e sinalizadores estabelecem uma sessão MAPI.
  
**MAPI session flowchart**
  
![Fluxograma de sessão MAPI](media/amapi_47.gif "MAPI")
  
Para obter informações sobre como lidar com sessões de dentro de um aplicativo cliente, consulte [Tratamento de Sessão MAPI](mapi-session-handling.md)
  
## <a name="see-also"></a>Confira também

- [MAPILogonEx](mapilogonex.md)  
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [Manipulação de sessão MAPI](mapi-session-handling.md)  
- [Visão geral da programação MAPI](mapi-programming-overview.md)

