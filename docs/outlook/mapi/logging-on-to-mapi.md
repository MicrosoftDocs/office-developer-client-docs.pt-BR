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
  
Os aplicativos cliente fazem logon no subsistema MAPI chamando a função **funçãomapilogonex** . Para obter mais informações, consulte [funçãomapilogonex](mapilogonex.md). **Funçãomapilogonex** valida a seleção de perfil e a configuração de cada provedor de serviços no perfil. Depois de configurado, o MAPI inicia os provedores de catálogo de endereços antes de iniciar os provedores de repositório de mensagens. Os provedores de transporte são iniciados quando seus serviços são exigidos pela primeira vez. 
  
## <a name="choose-a-profile"></a>Escolha um perfil
  
- Passe uma cadeia de caracteres que representa o nome do perfil no parâmetro _lpszProfileName_ para **funçãomapilogonex**ou...
    
- Permitir que o usuário especifique o perfil passando nulo no parâmetro _lpszProfileName_ e definindo o sinalizador MAPI_LOGON_UI ou... 

- Selecione o perfil padrão passando nulo no parâmetro _lpszProfileName_ e definindo o sinalizador MAPI_USE_DEFAULT. 
    
Se você precisar de um perfil específico que não seja o padrão, deverá salvar seu nome no seu próprio banco de dados de configuração ou usar uma Convenção de nomenclatura específica. MAPI não expõe nenhum atributo de perfil diferente do nome e sinalizador padrão na tabela de perfil, e o sinalizador de perfil padrão é reservado para o cliente de mensagens e aplicativos IPM relacionados.
  
Os clientes que fornecem o perfil parcial ou as informações de configuração do provedor para **funçãomapilogonex** devem solicitar ao usuário os dados adicionais, permitindo que uma caixa de diálogo seja exibida. Se as informações estiverem ausentes e o **funçãomapilogonex** não puder solicitar que o usuário a forneça, o logon falhará. Os clientes que não precisam de entrada do usuário podem suprimir a exibição da caixa de diálogo. 
  
Os sinalizadores que o **funçãomapilogonex** usa para habilitar uma interface do usuário são mutuamente exclusivos; somente um pode ser definido. Deixar esses sinalizadores desdefinidas suprime a exibição de uma interface do usuário, fazendo com que o **funçãomapilogonex** falhe se as informações necessárias estiverem ausentes. Ou seja, se você desabilitar a interface do usuário e passar NULL para o parâmetro _lpszProfileName_ e não definir o sinalizador MAPI_USE_DEFAULT, **funçãomapilogonex** falhará porque não é possível recuperar um nome de perfil. 
  
A sessão que o **funçãomapilogonex** estabelece pode ser uma sessão de mensagens individual, uma sessão de mensagens compartilhada ou uma sessão de não-mensagens. As sessões de mensagens individuais são conexões privadas entre o cliente e o subsistema MAPI e podem ser estabelecidas Configurando o sinalizador MAPI_NEW_SESSION na chamada para **funçãomapilogonex**.
  
Sessões de mensagens comPartilhadas são conexões que vários clientes de mensagens podem usar. As sessões comPartilhadas normalmente são estabelecidas para clientes que usam o mesmo perfil. Para estabelecer uma nova sessão como uma sessão compartilhada, defina o sinalizador MAPI_ALLOW_OTHERS. 
  
## <a name="use-an-existing-shared-session"></a>Usar uma sessão compartilhada existente
  
- Não defina o sinalizador MAPI_NEW_SESSION.
    
- Não defina o sinalizador MAPI_ALLOW_OTHERS.
    
- Passe NULL para o parâmetro _lpszProfileName_ . 
    
- Passe NULL para o parâmetro _lpszPassword_ . 
    
As sessões de não envio de mensagens permitem que os clientes acessem o subsistema MAPI, mas não permitem que as mensagens sejam enviadas ou recebidas. Os aplicativos de configuração ou administração são exemplos de clientes que podem precisar estabelecer sessões de não-mensagens. Para solicitar uma sessão de não-mensagens, defina o sinalizador MAPI_NO_MAIL. A configuração desse sinalizador faz o logon do cliente sem informar o spooler MAPI. Os clientes que fazem logon em MAPI com esse sinalizador não podem esperar nunca receber relatórios de status de leitura.
  
O sinalizador MAPI_NO_MAIL deve ser definido somente:
  
- Se o cliente não enviará ou receberá mensagens durante a sessão.
    
- Se o cliente tem controle completo sobre o conteúdo do perfil e as mensagens são enviadas e recebidas usando o repositório de mensagens rigidamente acoplado e provedores de transporte, como os provedores do Microsoft Exchange.
    
Um cliente de mensagens pode compartilhar uma sessão com um cliente que não seja de mensagens. As características de um membro de uma sessão compartilhada não são afetadas pelas características de outros membros. Ou seja, se você fizer logon com os sinalizadores MAPI_NO_MAIL e MAPI_ALLOW_OTHERS definidos, um cliente de mensagens que fizer logon na sua sessão não afetará a operação do cliente e vice-versa. O cliente de mensagens ainda poderá enviar e receber mensagens e seu cliente não.
  
**Funçãomapilogonex** define alguns outros sinalizadores que você pode definir: 
  
- MAPI_FORCE_DOWNLOAD indica que as mensagens de entrada devem ser baixadas antes que o **funçãomapilogonex** retorne. A não definição desse sinalizador faz com que as mensagens sejam baixadas em segundo plano posteriormente. 
    
- O MAPI_SERVICE_UI_ALWAYS solicita que todos os serviços de mensagens no perfil exibam uma caixa de diálogo de configuração.
    
- MAPI_NT_SERVICE indica que o cliente é implementado como um serviço do Windows. Esse sinalizador deverá ser definido se o cliente for um serviço.
    
Com cada logon bem-sucedido, **funçãomapilogonex** retorna um ponteiro para uma sessão MAPI. Você pode usar esse ponteiro para chamar os métodos da interface **IMAPISession** . Para obter mais informações, consulte [IMAPISession: IUnknown](imapisessioniunknown.md). Os ponteiros de sessão, independentemente do tipo de sessão, são exclusivos dos clientes que os recebem e não são válidos nas tarefas.
  

