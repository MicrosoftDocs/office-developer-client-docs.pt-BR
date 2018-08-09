---
title: Sessões MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c5a7c137-393e-40ff-a2b9-afe02da2435a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 45dc993c337249ed7d4dffbd5324267de82981d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767951"
---
# <a name="mapi-sessions"></a>Sessões MAPI

**Aplica-se a**: Outlook 
  
Antes do aplicativo cliente pode chamar um sistema de mensagens subjacente, ele precisa estabelecer uma sessão ou conexão, com o subsistema MAPI.
  
Sessões são iniciadas quando um usuário faz logon, um processo que acessa um perfil válido e valida o sistema de mensagens e as credenciais do serviço de mensagem. Em seguida, o processo garante que todos os serviços de mensagem do perfil estão configurados corretamente. A interface de cliente que você usa determina a chamada de logon. Clientes MAPI chamar a função de [MAPILogonEx](mapilogonex.md) . 
  
Configuração do serviço de mensagens é uma das partes mais importantes do processo de logon. O perfil é a origem inicial das informações de configuração. Se informações sobre um serviço de mensagem específica estiverem ausentes, o processo de logon tenta solicitar ao usuário para fornecer a ele. Isso nem sempre é bem-sucedida por dois motivos: primeiro, solicitando que o usuário requer a exibição de uma caixa de diálogo. É possível para que os clientes não permitir a exibição de uma interface do usuário, passando um sinalizador na chamada de logon. Em segundo lugar, o usuário pode cancelar a caixa de diálogo antes que as informações necessárias podem ser adicionadas.
  
Quando um processo de logon falha uma vez, o usuário é informado sobre a falha e tem a chance de repetição ou corrigir a condição de erro. Mais uma vez, uma interface de usuário será exibida, se o cliente permite e o usuário será solicitado a inserir quaisquer dados estão faltando. Se esse segundo try for bem sucedida, MAPI desabilita todos os provedores de serviço no serviço de mensagem para a duração da sessão. Na verdade, o serviço de mensagem inteira está desabilitado. Isso significa que nenhum dos provedores de serviço no serviço de mensagem pode trabalhar. Isso é feito porque se um provedor de falha de logon, os outros provedores geralmente também falharem. O processo de logon pode falhar devido a um caminho inválido para um recurso necessário, uma versão incompatível do MAPI, um servidor de mensagens não está disponível ou corrupção de dados. 
  
Os clientes podem especificar um dos dois tipos de sessões seja estabelecida na chamada logon: uma sessão individual ou uma sessão compartilhada. Sessões individuais são conexões particulares; Há um relacionamento individual entre um aplicativo cliente e a sessão está usando. Como consequência, aplicativos de cliente que compartilham uma sessão também compartilham um perfil. Sessões compartilhadas são estabelecidas uma vez, mas podem ser usadas por outros aplicativos cliente que precisam usá-los. O perfil e as credenciais são especificadas somente com o logon inicial. 
  
Os clientes podem fazer logon várias vezes como o mesmo usuário ou vários usuários. MAPI não impede a isso. Alguns provedores de serviços, no entanto, podem não ser tão flexíveis, retornando o valor de erro MAPI_E_SESSION_LIMIT em tentativas de logon subsequentes. Provedores de serviços com limitações de hardware subjacente podem ser necessária para impor um limite de sessão.
  
As chamadas de função para o estabelecimento de uma sessão tem uma coleção de parâmetros e os sinalizadores que controlam como a sessão é criada. O cliente especifica um nome de perfil opcional e um identificador de janela que atua como a janela pai para as caixas de diálogo que são exibidos. Os sinalizadores incluem MAPI_NEW_SESSION, que solicita que uma nova sessão individual (em vez de uma sessão compartilhada) ser estabelecida, e o sinalizador de interface do usuário MAPI_LOGON_UI. O sinalizador de interface do usuário é definido como solicitar uma caixa de diálogo de logon.
  
A ilustração a seguir mostra como esses parâmetros e os sinalizadores vários estabelecem uma sessão MAPI.
  
**MAPI session flowchart**
  
![Fluxograma de sessão MAPI] (media/amapi_47.gif "Fluxograma de sessão MAPI")
  
Para obter informações sobre como lidar com sessões de dentro de um aplicativo cliente, consulte [Manipulação de sessão MAPI](mapi-session-handling.md)
  
## <a name="see-also"></a>Confira também

- [MAPILogonEx](mapilogonex.md)  
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [Tratamento de sessão MAPI](mapi-session-handling.md)  
- [Vis�o geral da programa��o MAPI](mapi-programming-overview.md)

