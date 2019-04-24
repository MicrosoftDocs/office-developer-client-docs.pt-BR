---
title: IMSProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Logon
api_type:
- COM
ms.assetid: 890d9cbe-3570-4cf0-aeae-667c0e5ba181
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9c7f62c69c7a06f7ca0e4bfddcf789cddc536ea6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309664"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra o MAPI em uma instância de um provedor de armazenamento de mensagens.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG FAR * lpcbSpoolSecurity,
  LPBYTE FAR * lppbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parâmetros

 _lpMAPISup_
  
> no Um ponteiro para o objeto de suporte MAPI atual para o repositório de mensagens.
    
 _ulUIParam_
  
> no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido. 
    
 _lpszProfileName_
  
> no Um ponteiro para uma cadeia de caracteres que contém o nome do perfil que está sendo usado para o logon do provedor de armazenamento. Essa cadeia de caracteres pode ser exibida em caixas de diálogo, gravadas em um arquivo de log ou simplesmente ignorada. Ele deve estar no formato Unicode se o sinalizador MAPI_UNICODE estiver definido no parâmetro _parâmetroulflags_ . 
    
 _cbEntryID_
  
> no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada para o repositório de mensagens. Passar **NULL** no _lpEntryID_ indica que um repositório de mensagens ainda não foi selecionado e que as caixas de diálogo que permitem que o usuário selecione um repositório de mensagens pode ser apresentado. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o logon é executado. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> A chamada terá permissão para ter êxito, mesmo se o objeto subjacente não estiver disponível para a implementação de chamada. Se o objeto não estiver disponível, uma chamada subsequente para o objeto poderá gerar um erro.
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se MAPI_UNICODE não for definido, as cadeias de caracteres estarão no formato ANSI.
    
MDB_NO_DIALOG 
  
> Impede a exibição de caixas de diálogo de logon. Se esse sinalizador estiver definido, o valor de erro MAPI_E_LOGON_FAILED será retornado se o logon não tiver êxito. Se esse sinalizador não for definido, o provedor de armazenamento de mensagens poderá solicitar que o usuário corrija um nome ou senha, insira um disco ou execute outras ações necessárias para estabelecer conexão com o repositório.
    
MDB_NO_MAIL 
  
> O repositório de mensagens não deve ser usado para enviar ou receber emails. O sinalizador sinaliza que o MAPI não notifique o spooler MAPI que este repositório de mensagens está sendo aberto. Se esse sinalizador estiver definido e o repositório de mensagens estiver rigidamente acoplado a um provedor de transporte, o provedor não precisará chamar o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) . 
    
MDB_TEMPORARY 
  
> Faz logon no repositório para que as informações possam ser recuperadas programaticamente da seção perfil, sem o uso de caixas de diálogo. Esse sinalizador instrui o MAPI de que o repositório não deve ser adicionado à tabela do repositório de mensagens e que o repositório não pode tornar-se permanente. Se esse sinalizador estiver definido, os provedores do repositório de mensagens não precisarão chamar o método [IMAPISupport:: ModifyProfile](imapisupport-modifyprofile.md) . 
    
MDB_WRITE 
  
> Solicita permissão de leitura/gravação.
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) do repositório de mensagens para fazer logon no. Passar **NULL** indica que a interface MAPI para o repositório de mensagens ( [IMsgStore](imsgstoreimapiprop.md)) é retornada. O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o repositório de mensagens (por exemplo, IID_IUnknown ou IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> bota Um ponteiro para a variável na qual o provedor de repositório retorna o tamanho, em bytes, dos dados de validação no parâmetro _lppbSpoolSecurity_ . 
    
 _lppbSpoolSecurity_
  
> bota Um ponteiro para o ponteiro para os dados de validação retornados. Esses dados de validação são fornecidos para que o método [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md) possa registrar o spooler MAPI no mesmo repositório do provedor de armazenamento de mensagens. 
    
 _lppMAPIError_
  
> bota Um ponteiro para um ponteiro para a estrutura [MAPIERROR](mapierror.md) retornada, se houver, que contenha informações de versão, componente e contexto de um erro. O parâmetro _lppMAPIError_ pode ser definido como **NULL** se não houver nenhuma estrutura **MAPIERROR** a ser retornada. 
    
 _lppMSLogon_
  
> bota Um ponteiro para o ponteiro para o objeto de logon do repositório de mensagens para MAPI para fazer logon no.
    
 _lppMDB_
  
> bota Um ponteiro para o ponteiro para o objeto do repositório de mensagens para o spooler MAPI e aplicativos cliente para fazer logon no.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_FAILONEPROVIDER 
  
> Este provedor não pode fazer logon, mas esse erro não deve desabilitar o serviço. 
    
MAPI_E_LOGON_FAILED 
  
> Não foi possível estabelecer uma sessão de logon.
    
MAPI_E_UNCONFIGURED 
  
> O perfil não contém informações suficientes para que o logon seja concluído. Quando esse valor é retornado, MAPI chama a função de ponto de entrada do provedor de repositório de mensagens.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
MAPI_E_UNKNOWN_CPID 
  
> O servidor não está configurado para dar suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> O servidor não está configurado para dar suporte às informações de localidade do cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada teve êxito, mas o provedor do repositório de mensagens tem informações de erro disponíveis. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md). Para obter as informações de erro do provedor, chame o método [IMAPISession:: GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Comentários

MAPI chama o método **IMSProvider:: logon** para fazer a maioria dos processamentos necessários para obter acesso a um repositório de mensagens. Os provedores de repositórios de mensagens validam quaisquer credenciais de usuário necessárias para acessar um determinado repositório e retornar um objeto de repositório de mensagens no parâmetro _lppMDB_ que o spooler MAPI e os aplicativos cliente podem fazer logon. 
  
Além do objeto de repositório de mensagens retornado para uso do cliente e do spooler MAPI, o provedor também retorna um objeto de logon do repositório de mensagens para MAPI usar no controle do repositório aberto. O objeto de logon do repositório de mensagens e o objeto do repositório de mensagens devem ser vinculados rigidamente dentro do provedor de armazenamento de mensagens para que cada um possa afetar o outro. O uso do objeto Store e o objeto logon devem ser idênticos; deve haver uma correspondência de um para um entre o objeto de logon e o objeto Store, de forma que os objetos atuem como se fossem um objeto que expõe duas interfaces. Os dois objetos também devem ser criados juntos e liberados juntos. 
  
O objeto de suporte MAPI, criado por MAPI e passado para o provedor no parâmetro _lpMAPISup_ , fornece acesso a funções no MAPI que o provedor requer. Elas incluem funções que salvam e recuperam informações de perfil, catálogos de endereços de acesso e assim por diante. O ponteiro _lpMAPISup_ pode ser diferente para cada loja aberto. Durante o processamento de chamadas para um repositório de mensagens após o logon, o provedor de repositório deve usar a variável _lpMAPISup_ específica desse repositório. Para qualquer chamada de **logon** que abra um repositório de mensagens e tenha êxito na criação de um objeto de logon do repositório de mensagens, o provedor deve salvar um ponteiro para o objeto de suporte MAPI no objeto de logon de repositório e deve chamar o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para adicionar uma referência para o objeto support. 
  
O parâmetro _ulUIParam_ deve ser usado se o provedor apresentar caixas de diálogo durante a chamada de **logon** . No enTanto, as caixas de diálogo não devem ser apresentadas se _parâmetroulflags_ contiver o sinalizador MDB_NO_DIALOG. Se uma interface do usuário precisa ser chamada, mas o _parâmetroulflags_ não a permite, ou se, por algum motivo, uma interface do usuário não pode ser exibida, o provedor deve retornar MAPI_E_LOGON_FAILED. Se o **logon** exibir uma caixa de diálogo e o usuário cancelar o logon, geralmente clicando no botão **Cancelar** da caixa de diálogo, o provedor deverá retornar MAPI_E_USER_CANCEL. 
  
O parâmetro _lpEntryID_ pode ser **nulo** ou apontar para um identificador de entrada de repositório desempacotado que esse repositório de mensagens criou anteriormente. Se _lpEntryID_ apontar para um identificador de entrada não delimitado, esse identificador de entrada poderá vir de um dos vários locais: 
  
- Pode ser um identificador de entrada que o provedor de armazenamento encapsulava anteriormente e escreveu na seção de perfil como uma propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
- Pode ser um identificador de entrada que o provedor anteriormente encontrava e retornou a um cliente de chamada como uma propriedade **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). 
    
- Pode ser um identificador de entrada que o provedor encontrava anteriormente e retornou a um cliente de chamada como a propriedade **PR_ENTRYID** de um objeto de repositório de mensagens. 
    
Em qualquer um desses casos, é possível que o identificador de entrada tenha sido criado em um computador diferente daquele que está sendo usado no momento.
  
Quando _lpEntryID_ não é **nulo**, ele deve conter todas as informações necessárias para identificar e localizar o repositório de mensagens. Essas informações podem incluir nomes de volume de rede, números de telefone, nomes de contas de usuário e assim por diante. Se a conexão com o repositório não puder ser feita usando os dados no identificador de entrada, o provedor de repositório deverá exibir uma caixa de diálogo que permite ao usuário selecionar o repositório a ser aberto. Uma caixa de diálogo pode ser necessária, por exemplo, se um servidor tiver sido renomeado, um nome de conta tiver sido alterado ou partes da rede não estiverem disponíveis.
  
Quando _lpEntryID_ é **nulo**, o repositório de mensagens a ser usado ainda não foi selecionado. O provedor ainda pode acessar um repositório sem exibir uma caixa de diálogo se ele oferecer suporte a outros métodos para especificar o repositório. Por exemplo, o provedor pode verificar seu arquivo de inicialização ou pode procurar propriedades adicionais que foram colocadas em sua seção de perfil do serviço de mensagens na configuração.
  
Se um provedor descobrir que todas as informações necessárias não estão no perfil, ele deve retornar MAPI_E_UNCONFIGURED. O MAPI chamará a função de ponto de entrada do serviço de mensagens do provedor para permitir que o usuário selecione um repositório ou até mesmo crie um, e insira um nome de conta e uma senha, conforme necessário. MAPI cria automaticamente uma nova seção de perfil para uma nova loja; Esta nova seção de perfil pode ser temporária ou permanente, dependendo de como ele foi adicionado. Se o provedor de repositório chamar o método **IMAPISupport:: ModifyProfile** , a nova seção de perfil se tornará permanente e a loja será adicionada à lista de repositórios de mensagens retornada pelo método [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
O parâmetro _lpInterface_ especifica a IID da interface necessária para o objeto do repositório recentemente aberto. Passar **NULL** no _lpInterface_ especifica que a interface de armazenamento de mensagens MAPI, **IMsgStore**, é necessária. Passar o objeto Message Store, IID_IMsgStore, também especifica que **IMsgStore** é necessário. Se IID_IUnknown for passado no _lpInterface_, o provedor deverá abrir o repositório usando qualquer interface derivada de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) é melhor para o provedor (novamente, isso geralmente é **IMsgStore**). Quando IID_IUnknown é passado, a implementação de chamada usa o método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para selecionar uma interface após a operação de abertura do repositório ter êxito. 
  
A chamada **IMSProvider:: logon** deve retornar informações suficientes, como um caminho para o repositório e as credenciais para acessar o repositório, para permitir que o spooler MAPI faça logon no mesmo repositório que o provedor de armazenamento não apresente uma caixa de diálogo. Os parâmetros _lpcbSpoolSecurity_ e _lppbSpoolSecurity_ são usados para retornar essas informações. O provedor aloca a memória para esses dados passando um ponteiro para um buffer no parâmetro _lpfAllocateBuffer_ da função [MSProviderInit](msproviderinit.md) ; o provedor coloca o tamanho desse buffer no _lpcbSpoolSecurity_. 
  
O MAPI libera esse buffer quando apropriado. Se o logon do MAPI spooler no repositório puder ser feito a partir das informações na seção perfil, o provedor poderá retornar nulo em _lppbSpoolSecurity_ e 0 para o tamanho da informação no _lpcbSpoolSecurity_. O logon do spooler MAPI ocorre como parte de um processo diferente do logon da loja; como o buffer que contém as informações passadas é copiado entre os processos, ele pode não estar na memória no mesmo local para o processo de spooler de MAPI para o processo de provedor de repositório. Portanto, um provedor não deve colocar endereços nesse buffer. Para obter mais informações sobre o logon do spooler MAPI, consulte o método [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md) . 
  
A maioria dos provedores de repositórios usa o método [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) do objeto support passado no parâmetro _lpMAPISup_ para salvar e recuperar as credenciais e opções do usuário. O **OpenProfileSection** permite que um provedor de armazenamento Salve informações arbitrárias adicionais em uma seção de perfil e a associe a um recurso específico. Por exemplo, um provedor de repositório pode salvar o nome da conta de usuário e a senha associada a um recurso e quaisquer caminhos ou outras informações necessárias para acessar esse recurso. 
  
Propriedades com identificadores de propriedade 0x6600 a 0x67FF são propriedades seguras disponíveis para o provedor de seu próprio uso para armazenar dados particulares em seções de perfil. Para obter mais informações sobre os usos de propriedades nos objetos seção de perfil, consulte o método [IProfSect: IMAPIProp](iprofsectimapiprop.md) . 
  
Além de qualquer dado privado em Propriedades com identificadores 0x6600 a 0x67FF, o provedor de repositório deve fornecer informações para a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) em sua seção de perfil. Ele deve colocar no **PR_DISPLAY_NAME** o nome de exibição do próprio provedor — uma cadeia de caracteres de identificação (por exemplo, "repositório de informações pessoais da Microsoft") que é exibida aos usuários para que eles possam distinguir o repositório de mensagens de outras pessoas que podem ter acesso Para. **PR_DISPLAY_NAME** normalmente contém um nome de servidor, nome de conta de usuário ou caminho. 
  
Algumas propriedades de seção de perfil estão visíveis na tabela do repositório de mensagens; outras estão visíveis durante a instalação, instalação e configuração do subsistema MAPI. O provedor geralmente fornece informações para essas propriedades visíveis para uma nova seção de perfil, que ainda não inclui credenciais ou informações privadas salvas, e quando descobre que as informações da propriedade foram alteradas. Para obter mais informações sobre seções de perfil, consulte [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md).
  
Após o logon bem-sucedido de um usuário e antes de retornar ao MAPI, o provedor de repositório deve criar a matriz de propriedades para a linha de status do recurso e chamar o método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) . 
  
 As chamadas de **logon** que abrem repositórios de mensagens que já estão abertas para a sessão MAPI atual ignoram grande parte do processamento descrito anteriormente. Essas chamadas não criam linhas de status, retornam objetos de logon do repositório de mensagens, chamam **AddRef** para o objeto de suporte MAPI ou retornam dados para o logon do spooler MAPI. Essas chamadas retornam S_OK e retornam um objeto de repositório de mensagens com a interface solicitada. 
  
Para detectar essas chamadas, o provedor deve manter uma lista no objeto do provedor de repositório de mensagens já aberto para este objeto Provider. Ao processar uma chamada de **logon** , o provedor deve verificar esta lista de repositórios abertos e determinar se o repositório a ser conectado já está aberto. Se for, as credenciais do usuário não precisam ser verificadas e a exibição de uma caixa de diálogo deve ser evitada, se possível. Se as caixas de diálogo devem ser exibidas, o provedor deve verificar as informações retornadas para ver se um repositório foi aberto uma segunda vez. Além disso, o provedor deve verificar se há aberturas duplicadas usando o _lpEntryID_ no início do processamento de chamadas de **logon** . 
  
O processamento padrão para uma chamada de **logon** que acessa um repositório aberto é o seguinte: 
  
1. O provedor de repositório chama **AddRef** para o objeto Store existente se a nova interface que está sendo solicitada for a mesma que a interface para o repositório existente. Caso contrário, ele chamará **QueryInterface** para obter a nova interface. Se o repositório não oferecer suporte à nova interface, o provedor deverá retornar o valor de erro MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. O provedor retorna um ponteiro para a interface necessária do objeto Store existente no _lppMDB_.
    
3. O provedor retorna **nulo** no _lppMSLogon_.
    
4. O provedor não deve abrir o perfil do objeto de suporte passado na chamada. Além disso, ele não deve registrar um identificador exclusivo de provedor, registrar uma linha de status ou retornar dados de Logon MAPI spooler.
    
5. O provedor não deve chamar **AddRef** para o objeto support, pois não requer um ponteiro para o objeto. 
    
Sempre que possível, os provedores devem retornar cadeias de caracteres de erro e de aviso apropriadas para chamadas de **logon** , pois isso facilita muito a carga dos usuários em determinar por que algo não funcionou. Para retornar essas cadeias de caracteres, um provedor define os membros na estrutura **MAPIERROR** . MAPI procura, usa e libera a estrutura **MAPIERROR** se for retornado por um provedor. 
  
A memória para esta estrutura **MAPIERROR** deve ser alocada usando o buffer passado no _LpfAllocateBuffer_ na chamada **MSProviderInit** . Qualquer cadeia de caracteres de erro contida na estrutura retornada deve estar no formato Unicode se MAPI_UNICODE estiver definido no **logon** _parâmetroulflags;_ caso contrário, ele deve estar no conjunto de caracteres ANSI. 
  
Para a maioria dos valores de erro retornados do **logon**, o MAPI desabilita os serviços de mensagens aos quais o provedor com falha pertence. O MAPI não chamará nenhum provedor que pertença a esses serviços pela vida da sessão MAPI. Por outro lado, quando o **logon** retorna o valor de erro MAPI_E_FAILONEPROVIDER de seu logon, o MAPI não desabilita o serviço de mensagens ao qual o provedor pertence. O **logon** deverá retornar MAPI_E_FAILONEPROVIDER se encontrar um erro que não garante a desabilitação de todo o serviço durante a vigência da sessão. Por exemplo, um provedor pode retornar esse erro quando não permite a exibição de uma interface de usuário e uma senha necessária não está disponível. 
  
Se um provedor retornar MAPI_E_UNCONFIGURED de seu logon, o MAPI chamará a função de entrada do serviço de mensagens do provedor e, em seguida, repetirá o logon. O MAPI passa MSG_SERVICE_CONFIGURE como o contexto para dar ao serviço a oportunidade de configurá-lo. Se o cliente optou por permitir uma interface de usuário no logon, o serviço pode apresentar sua folha de propriedades de configuração para que o usuário possa inserir informações de configuração.
  
## <a name="see-also"></a>Confira também



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md)
  
[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
  
[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MSProviderInit](msproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

