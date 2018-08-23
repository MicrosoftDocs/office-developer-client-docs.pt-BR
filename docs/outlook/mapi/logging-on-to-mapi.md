---
title: Fazer logon no MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 63f71066b1afc90c3e495ed4f9ba654bcbdfe558
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579925"
---
# <a name="logging-on-to-mapi"></a>Fazer logon no MAPI
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aplicativos cliente faça logon no subsistema de MAPI chamando a função **MAPILogonEx** . Para obter mais informações, consulte [MAPILogonEx](mapilogonex.md). **MAPILogonEx** valida a seleção de perfil e a configuração de cada provedor de serviços no perfil. Uma vez configurado, o MAPI inicia os provedores de catálogo de endereços antes de iniciar os provedores de repositório de mensagem. Provedores de transporte são iniciadas quando seus serviços primeiro são necessários. 
  
## <a name="choose-a-profile"></a>Escolha um perfil
  
- Passe em uma cadeia de caracteres que representa o nome do perfil no parâmetro _lpszProfileName_ para **MAPILogonEx**, ou …
    
- Permitir que o usuário especificar o perfil passar NULL no parâmetro _lpszProfileName_ e definindo o sinalizador MAPI_LOGON_UI, ou … 

- Selecione o perfil padrão passar NULL no parâmetro _lpszProfileName_ e definindo o sinalizador MAPI_USE_DEFAULT. 
    
Se você precisar de um perfil específico que não seja o perfil padrão, você deve salvar o seu nome em seu próprio banco de dados de configuração ou usar uma convenção de nomenclatura específica. MAPI não expõe os atributos de perfil que não seja o sinalizador de nome e padrão na tabela de perfil e o sinalizador de perfil padrão é reservado para mensagens de cliente e aplicativos de IPM relacionados.
  
Clientes que forneçam perfil parcial ou informações de configuração de provedor para **MAPILogonEx** devem avisar o usuário para os dados adicionais, permitindo que uma caixa de diálogo a ser exibido. Se estiver faltando informações e **MAPILogonEx** não pode solicitar o usuário a fornecer a ele, o logon falhará. Clientes que faça a necessidade de entrada do usuário não podem suprimir a exibição da caixa de diálogo. 
  
Os sinalizadores **MAPILogonEx** usa para habilitar uma interface do usuário são mutuamente exclusivos; apenas um pode ser definido. Deixar esses sinalizadores não definidas suprime a exibição de uma interface de usuário, causando **MAPILogonEx** falhe se estiver faltando informações necessárias. Ou seja, se você desativar a interface de usuário e passa nulo para o parâmetro _lpszProfileName_ e não definir o sinalizador MAPI_USE_DEFAULT, **MAPILogonEx** falhará porque ele não é possível recuperar um nome de perfil. 
  
A sessão que estabelece **MAPILogonEx** pode ser uma sessão de mensagens individual, uma sessão de mensagens compartilhada ou uma sessão nonmessaging. Sessões de mensagens individuais são privadas conexões entre o cliente e o subsistema MAPI e podem ser estabelecidas, definindo o sinalizador MAPI_NEW_SESSION na chamada a **MAPILogonEx**.
  
Sessões de mensagens compartilhadas são conexões que vários clientes de mensagens podem usar. Sessões compartilhadas geralmente são estabelecidas para os clientes usam o mesmo perfil. Para estabelecer uma nova sessão como uma sessão compartilhada, defina o sinalizador MAPI_ALLOW_OTHERS. 
  
## <a name="use-an-existing-shared-session"></a>Usar uma sessão compartilhada existente
  
- Não defina o sinalizador MAPI_NEW_SESSION.
    
- Não defina o sinalizador MAPI_ALLOW_OTHERS.
    
- Passe nulo para o parâmetro _lpszProfileName_ . 
    
- Passe nulo para o parâmetro _lpszPassword_ . 
    
Sessões nonmessaging permitir que os clientes acessar o subsistema de MAPI, mas não permitir mensagens a ser enviado ou recebido. Configuração ou administração de aplicativos são exemplos de clientes que talvez seja necessário para estabelecer sessões nonmessaging. Para solicitar uma sessão nonmessaging, defina o sinalizador MAPI_NO_MAIL. Defina esse sinalizador fará logon seu cliente sem informar o spooler MAPI. Clientes que faça logon MAPI com esse sinalizador não podem esperar nunca receber relatórios de status de leitura.
  
O sinalizador MAPI_NO_MAIL só deve ser definido:
  
- Se o seu cliente não será enviar ou receber mensagens durante a sessão.
    
- Se seu cliente tem controle total sobre o conteúdo do perfil e mensagens são enviadas e recebidas usando ligação estreita repositório de mensagem e transporte provedores, como os provedores do Microsoft Exchange.
    
Um cliente de mensagens pode compartilhar uma sessão com um cliente nonmessaging. As características de um membro de uma sessão compartilhada não são afetadas pelas características de outros membros. Ou seja, se você fizer logon com o conjunto de sinalizadores MAPI_NO_MAIL e MAPI_ALLOW_OTHERS, um cliente de mensagens logon à sua sessão não tem efeito sobre a operação de seu cliente e vice-versa. O cliente de mensagens ainda será possível enviar e receber mensagens e seu cliente não estará.
  
**MAPILogonEx** define alguns outros sinalizadores que podem ser definidos: 
  
- MAPI_FORCE_DOWNLOAD indica que as mensagens de entrada devem ser baixadas antes **MAPILogonEx** retorna. Não defina esse sinalizador faz com que as mensagens a serem baixadas em segundo plano mais tarde. 
    
- MAPI_SERVICE_UI_ALWAYS solicita que cada serviço de mensagem no perfil exibir uma caixa de diálogo de configuração.
    
- MAPI_NT_SERVICE indica que seu cliente é implementado como um serviço do Windows. Esse sinalizador deve ser definida se seu cliente for um serviço.
    
Com cada logon bem-sucedido, **MAPILogonEx** retorna um ponteiro para uma sessão MAPI. Você pode usar esse ponteiro para chamar os métodos da interface **IMAPISession** . Para obter mais informações, consulte [IMAPISession: IUnknown](imapisessioniunknown.md). Ponteiros de sessão, independentemente do tipo de sessão, são exclusivos para os clientes que recebem-las e não são válidos nas tarefas.
  

