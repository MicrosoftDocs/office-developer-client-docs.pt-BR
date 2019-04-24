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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319577"
---
# <a name="mapi-sessions"></a>Sessões MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes que o aplicativo cliente possa chamar um sistema de mensagens subjacente, ele deve estabelecer uma sessão ou conexão com o subsistema MAPI.
  
As sessões são iniciadas quando um usuário faz logon, um processo que acessa um perfil válido e valida o sistema de mensagens e as credenciais do serviço de mensagens. Em seguida, o processo garante que todos os serviços de mensagens do perfil estejam configurados corretamente. A interface de cliente usada determina a chamada de logon. Os clientes MAPI chamam a função [funçãomapilogonex](mapilogonex.md) . 
  
A configuração do serviço de mensagens é uma das partes mais importantes do processo de logon. O perfil é a fonte inicial para informações de configuração. Se as informações de um determinado serviço de mensagens estiverem ausentes, o processo de logon tentará solicitar que o usuário a forneça. Isso nem sempre é bem-sucedido por dois motivos: primeiro, avisar o usuário requer a exibição de uma caixa de diálogo. É possível que os clientes desautorizam a exibição de uma interface de usuário passando um sinalizador para a chamada de logon. Em segundo lugar, o usuário pode cancelar a caixa de diálogo para que as informações necessárias possam ser adicionadas.
  
Quando um processo de logon falha uma vez, o usuário é informado da falha e tem a chance de tentar novamente ou corrigir a condição de erro. Novamente, uma interface do usuário será exibida se o cliente permitir, e o usuário será solicitado a inserir os dados que estão ausentes. Se essa segunda tentativa não tiver êxito, o MAPI desabilita todos os provedores de serviço no serviço de mensagens durante a sessão. Na verdade, todo o serviço de mensagem é desabilitado. Isso significa que nenhum dos provedores de serviço no serviço de mensagens pode funcionar. Isso é feito porque, se um provedor falhar, os outros provedores também falharão. O processo de logon pode falhar devido a um caminho inválido para um recurso necessário, uma versão incompatível de MAPI, um servidor de mensagens não disponível ou corrupção de dados. 
  
Os clientes podem especificar um dos dois tipos de sessões a serem estabelecidas na chamada de logon: uma sessão individual ou uma sessão compartilhada. As sessões individuais são conexões privadas; Há uma relação um-para-um entre um aplicativo cliente e a sessão que está usando. Como consequência, os aplicativos clientes que compartilham uma sessão também compartilham um perfil. As sessões comPartilhadas são estabelecidas uma vez, mas podem ser usadas por outros aplicativos cliente que precisam usá-las. O perfil e as credenciais são especificados somente com o logon inicial. 
  
Os clientes podem fazer logon várias vezes como o mesmo usuário ou como vários usuários. O MAPI não impede isso. No entanto, alguns provedores de serviços podem não ser tão flexíveis, retornando o valor de erro MAPI_E_SESSION_LIMIT nas tentativas de logon subsequentes. Os provedores de serviços com limitações de hardware subjacentes podem ser necessários para impor um limite de sessão.
  
As chamadas de função para estabelecer uma sessão têm uma coleção de sinalizadores e parâmetros que controlam como a sessão é criada. O cliente especifica um nome de perfil opcional e um identificador de janela que atua como a janela pai para qualquer caixa de diálogo exibida. Os sinalizadores incluem MAPI_NEW_SESSION, que solicita que uma nova sessão individual (em vez de uma sessão compartilhada) seja estabelecida e o sinalizador de interface do usuário do MAPI_LOGON_UI. O sinalizador de interface do usuário é definido para solicitar uma caixa de diálogo de logon.
  
A ilustração a seguir mostra como esses vários parâmetros e sinalizadores estabelecem uma sessão MAPI.
  
**MAPI session flowchart**
  
![Fluxograma de sessão MAPI] (media/amapi_47.gif "Fluxograma de sessão MAPI")
  
Para obter informações sobre como lidar com sessões de dentro de um aplicativo cliente, consulte [MAPI Session Handling](mapi-session-handling.md)
  
## <a name="see-also"></a>Confira também

- [MAPILogonEx](mapilogonex.md)  
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [Manipulação de sessão MAPI](mapi-session-handling.md)  
- [Vis�o geral da programa��o MAPI](mapi-programming-overview.md)

