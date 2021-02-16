---
title: Fazer logon no MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cce43301ac73a5646e263b2ab92700e57804637d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419706"
---
# <a name="logging-on-to-mapi"></a>Fazer logon no MAPI
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente fazem logoff no subsistema MAPI chamando a **função MAPILogonEx.** Para obter mais informações, [consulte MAPILogonEx](mapilogonex.md). **O MAPILogonEx valida** a seleção de perfil e a configuração de cada provedor de serviços no perfil. Depois de configurado, o MAPI inicia os provedores de agendas antes de iniciar os provedores de armazenamento de mensagens. Os provedores de transporte são iniciados quando seus serviços são necessários pela primeira vez. 
  
## <a name="choose-a-profile"></a>Escolher um perfil
  
- Passe uma cadeia de caracteres que representa o nome do perfil no parâmetro  _lpszProfileName_ para **MAPILogonEx** ou...
    
- Permita que o usuário especifique o perfil passando NULL no parâmetro  _lpszProfileName_ e definindo o sinalizador MAPI_LOGON_UI, ou... 

- Selecione o perfil padrão passando NULL no parâmetro  _lpszProfileName_ e definindo o MAPI_USE_DEFAULT padrão. 
    
Se você precisar de um perfil específico diferente do perfil padrão, deverá salvar seu nome em seu próprio banco de dados de configuração ou usar uma convenção de nomenal específica. MAPI does not expose any profile attributes other than the name and default flag in the profile table, and the default profile flag is reserved for messaging client and related IPM applications.
  
Clientes que fornecem informações parciais de configuração de perfil ou provedor para **MAPILogonEx** devem solicitar ao usuário os dados adicionais, permitindo que uma caixa de diálogo seja exibida. Se as informações estão ausentes e **o MAPILogonEx não** pode solicitar que o usuário as fornegue, o logon falhará. Clientes que não precisam de entrada do usuário podem suprimir a exibição da caixa de diálogo. 
  
Os sinalizadores que **MAPILogonEx** usa para habilitar uma interface do usuário são mutuamente exclusivos; somente um pode ser definido. Deixar esses sinalizadores sem sinal suprime a exibição de uma interface do usuário, fazendo com que **MAPILogonEx** falhe se as informações necessárias não são fornecidas. Ou seja, se você desabilitar a interface do usuário e passar NULL para o parâmetro  _lpszProfileName_ e não definir o sinalizador MAPI_USE_DEFAULT, **o MAPILogonEx** falhará porque não é possível recuperar um nome de perfil. 
  
A sessão que **o MAPILogonEx** estabelece pode ser uma sessão de mensagens individual, uma sessão de mensagens compartilhada ou uma sessão não-desastrável. Sessões de mensagens individuais são conexões privadas entre seu cliente e o subsistema MAPI e podem ser estabelecidas definindo o sinalizador MAPI_NEW_SESSION na chamada para **MAPILogonEx**.
  
As sessões de mensagens compartilhadas são conexões que vários clientes de mensagens podem usar. As sessões compartilhadas geralmente são estabelecidas para que os clientes usem o mesmo perfil. Para estabelecer uma nova sessão como uma sessão compartilhada, de definida a MAPI_ALLOW_OTHERS configuração. 
  
## <a name="use-an-existing-shared-session"></a>Usar uma sessão compartilhada existente
  
- Não de definida a MAPI_NEW_SESSION sinalizador.
    
- Não de definida a MAPI_ALLOW_OTHERS sinalizador.
    
- Passe NULL para o _parâmetro lpszProfileName._ 
    
- Passe NULL para o _parâmetro lpszPassword._ 
    
As sessões não-desaessaria permitem que os clientes acessem o subsistema MAPI, mas não permitem que mensagens sejam enviadas ou recebidas. Aplicativos de configuração ou administração são exemplos de clientes que talvez precisem estabelecer sessões não-desessariamente. Para solicitar uma sessão que não seja desaessaria, de definida a MAPI_NO_MAIL configuração. A configuração desse sinalizador registra seu cliente sem informar o spooler MAPI. Clientes que se registram no MAPI com esse sinalizador não podem esperar receber relatórios de status de leitura.
  
O MAPI_NO_MAIL sinalizador só deve ser definido:
  
- Se o cliente não enviar ou receber mensagens durante a sessão.
    
- Se seu cliente tiver controle total sobre o conteúdo do perfil e as mensagens serão enviadas e recebidas usando provedores de transporte e armazenamento de mensagens fortemente a par, como os provedores do Microsoft Exchange.
    
Um cliente de mensagens pode compartilhar uma sessão com um cliente não-desaessariado. As características de um membro de uma sessão compartilhada não são afetadas pelas características de outros membros. Ou seja, se você fizer logon com os sinalizadores MAPI_NO_MAIL e MAPI_ALLOW_OTHERS definidos, um cliente de mensagens que faça logon em sua sessão não terá efeito sobre a operação do seu cliente e vice-versa. O cliente de mensagens ainda poderá enviar e receber mensagens, e seu cliente não.
  
**MAPILogonEx** define alguns outros sinalizadores que você pode definir: 
  
- MAPI_FORCE_DOWNLOAD indica que as mensagens de entrada devem ser baixadas antes que **MAPILogonEx seja** retornada. Não definir esse sinalizador faz com que as mensagens sejam baixadas em segundo plano posteriormente. 
    
- MAPI_SERVICE_UI_ALWAYS solicita que todos os serviços de mensagens no perfil exibem uma caixa de diálogo de configuração.
    
- MAPI_NT_SERVICE indica que seu cliente é implementado como um serviço do Windows. Esse sinalizador deve ser definido se o cliente for um serviço.
    
A cada logon bem-sucedido, **MAPILogonEx** retorna um ponteiro para uma sessão MAPI. Você pode usar esse ponteiro para chamar os métodos da interface **IMAPISession.** Para obter mais informações, [consulte IMAPISession : IUnknown](imapisessioniunknown.md). Ponteiros de sessão, independentemente do tipo de sessão, são exclusivos para os clientes que os recebem e não são válidos entre tarefas.
  

