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
  
Registra MAPI em uma instância de um provedor de armazenamento de mensagens.
  
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
  
> [in] Um ponteiro para o objeto de suporte MAPI atual para o armazenamento de mensagens.
    
 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. 
    
 _lpszProfileName_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém o nome do perfil que está sendo usado para logon do provedor de armazenamento. Essa cadeia de caracteres pode ser exibida em caixas de diálogo, escritas em um arquivo de log ou simplesmente ignoradas. Ele deverá estar no formato Unicode se o sinalizador MAPI_UNICODE estiver definido no _parâmetro ulFlags._ 
    
 _cbEntryID_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada para o armazenamento de mensagens. Passar **nulo**  _em lpEntryID_ indica que um armazenamento de mensagens ainda não foi selecionado e que as caixas de diálogo que permitem ao usuário selecionar um armazenamento de mensagens podem ser apresentadas. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o logon é realizado. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> A chamada tem permissão para ser bem-sucedida, mesmo se o objeto subjacente não estiver disponível para a implementação da chamada. Se o objeto não estiver disponível, uma chamada subsequente para o objeto poderá criar um erro.
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
MDB_NO_DIALOG 
  
> Impede a exibição de caixas de diálogo de logon. Se esse sinalizador estiver definido, o valor de erro MAPI_E_LOGON_FAILED será retornado se o logon não for bem-sucedido. Se esse sinalizador não estiver definido, o provedor do armazenamento de mensagens poderá solicitar que o usuário corrija um nome ou senha, insira um disco ou execute outras ações necessárias para estabelecer conexão com o armazenamento.
    
MDB_NO_MAIL 
  
> O armazenamento de mensagens não deve ser usado para enviar ou receber emails. O sinalizador sinaliza MAPI para não notificar o spooler MAPI de que esse armazenamento de mensagens está sendo aberto. Se esse sinalizador estiver definido e o armazenamento de mensagens estiver fortemente unido a um provedor de transporte, o provedor não precisará chamar o método [IMAPISupport::SpoolerNotify.](imapisupport-spoolernotify.md) 
    
MDB_TEMPORARY 
  
> Logs no armazenamento para que as informações possam ser recuperadas programaticamente da seção de perfil, sem o uso de caixas de diálogo. Esse sinalizador instrui o MAPI de que o armazenamento não deve ser adicionado à tabela do armazenamento de mensagens e que o armazenamento não pode se tornar permanente. Se esse sinalizador estiver definido, os provedores de armazenamento de mensagens não precisarão chamar o [método IMAPISupport::ModifyProfile.](imapisupport-modifyprofile.md) 
    
MDB_WRITE 
  
> Solicita permissão de leitura/gravação.
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador da interface) para o armazenamento de mensagens fazer logon. Passar **nulo** indica que a interface MAPI do repositório de mensagens ( [IMsgStore](imsgstoreimapiprop.md)) é retornada. O  _parâmetro lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o armazenamento de mensagens (por exemplo, IID_IUnknown ou IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> [out] Um ponteiro para a variável na qual o provedor de armazenamento retorna o tamanho, em bytes, dos dados de validação no _parâmetro lppbSpoolSecurity._ 
    
 _lppbSpoolSecurity_
  
> [out] Um ponteiro para o ponteiro para os dados de validação retornados. Esses dados de validação são fornecidos para que o método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) possa registrar o spooler MAPI no mesmo armazenamento que o provedor de armazenamento de mensagens. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a estrutura [MAPIERROR](mapierror.md) retornada, se alguma, que contenha informações de versão, componente e contexto para um erro. O  _parâmetro lppMAPIError_ pode ser definido como **nulo** se não houver **estrutura MAPIERROR** a ser retornada. 
    
 _lppMSLogon_
  
> [out] Um ponteiro para o ponteiro para o objeto de logon do armazenamento de mensagens para MAPI fazer logon.
    
 _lppMDB_
  
> [out] Um ponteiro para o ponteiro para o objeto de armazenamento de mensagens para o spooler MAPI e aplicativos cliente para fazer logoff.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_FAILONEPROVIDER 
  
> Este provedor não pode fazer logoff, mas esse erro não deve desabilitar o serviço. 
    
MAPI_E_LOGON_FAILED 
  
> Não foi possível estabelecer uma sessão de logon.
    
MAPI_E_UNCONFIGURED 
  
> O perfil não contém informações suficientes para que o logon seja concluído. Quando esse valor é retornado, o MAPI chama a função de ponto de entrada do serviço de mensagens do provedor de mensagens.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo. 
    
MAPI_E_UNKNOWN_CPID 
  
> O servidor não está configurado para dar suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> O servidor não está configurado para dar suporte às informações de localidade do cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas o provedor do armazenamento de mensagens tem informações de erro disponíveis. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md) Para obter as informações de erro do provedor, chame o [método IMAPISession::GetLastError.](imapisession-getlasterror.md) 
    
## <a name="remarks"></a>Comentários

O MAPI chama o método **IMSProvider::Logon** para fazer a maior parte do processamento necessário para obter acesso a um armazenamento de mensagens. Os provedores de armazenamento de mensagens validam qualquer credencial de usuário necessária para acessar um determinado armazenamento e retornar um objeto de armazenamento de mensagens no parâmetro  _lppMDB_ em que o spooler MAPI e os aplicativos cliente podem fazer logoff. 
  
Além do objeto de armazenamento de mensagens retornado para uso do spooler de cliente e MAPI, o provedor também retorna um objeto de logon do armazenamento de mensagens para o MAPI usar no controle do armazenamento aberto. O objeto de logon do armazenamento de mensagens e o objeto de armazenamento de mensagens devem estar fortemente vinculados dentro do provedor de armazenamento de mensagens para que cada um possa afetar o outro. O uso do objeto de armazenamento e do objeto de logon deve ser idêntico; deve haver uma correspondência um-para-um entre o objeto de logon e o objeto de armazenamento de forma que os objetos agem como se fosse um objeto que expõe duas interfaces. Os dois objetos também devem ser criados juntos e liberados juntos. 
  
O objeto de suporte MAPI, criado por MAPI e passado para o provedor no parâmetro  _lpMAPISup,_ fornece acesso a funções em MAPI que o provedor requer. Isso inclui funções que salvam e recuperam informações de perfil, acessar os livros de endereços e assim por diante. O  _ponteiro lpMAPISup_ pode ser diferente para cada armazenamento aberto. Durante o processamento de chamadas para um armazenamento de mensagens após o logon, o provedor de armazenamento deve usar a variável  _lpMAPISup_ específica para esse armazenamento. Para qualquer chamada de Logon que abre um armazenamento de mensagens e é bem-sucedida na criação de um objeto de **logon** do armazenamento de mensagens, o provedor deve salvar um ponteiro para o objeto de suporte MAPI no objeto de logon do armazenamento e deve chamar o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para adicionar uma referência para o objeto de suporte. 
  
O _parâmetro ulUIParam_ deve ser usado se o provedor apresentar caixas de diálogo durante a chamada **de logon.** No entanto, caixas de diálogo não devem ser  _apresentadas se ulFlags_ contiver o MDB_NO_DIALOG sinalizador. Se uma interface do usuário precisar ser chamada, mas  _ulFlags_ não permitir ou se, por algum outro motivo, uma interface do usuário não puder ser exibida, o provedor deverá retornar MAPI_E_LOGON_FAILED. Se **o logon** exibir uma caixa de diálogo e o usuário cancelar o  logon, normalmente clicando no botão Cancelar da caixa de diálogo, o provedor deverá retornar MAPI_E_USER_CANCEL. 
  
O  _parâmetro lpEntryID_ pode ser **nulo** ou apontar para um identificador de entrada de armazenamento não mapeado criado anteriormente por esse armazenamento de mensagens. Se  _lpEntryID_ aponta para um identificador de entrada não mapeada, esse identificador de entrada pode vir de um dos vários locais: 
  
- Pode ser um identificador de entrada que o provedor de armazenamento anteriormente baixou e escreveu na seção de perfil como uma **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) propriedade.
    
- Pode ser um identificador de entrada que o provedor anteriormente abalou e retornou a um cliente de chamada como uma **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) . 
    
- Pode ser um identificador de entrada que o provedor anteriormente abalou e retornou a um cliente de chamada como PR_ENTRYID **propriedade** de um objeto de armazenamento de mensagens. 
    
Em qualquer um desses casos, é possível que o identificador de entrada foi criado em um computador diferente do que está sendo usado no momento.
  
Quando  _lpEntryID_ não é **nulo**, ele deve conter todas as informações necessárias para identificar e localizar o armazenamento de mensagens. Essas informações podem incluir nomes de volume de rede, números de telefone, nomes de contas de usuário e assim por diante. Se a conexão com o armazenamento não puder ser feita usando os dados no identificador de entrada, o provedor do armazenamento deverá exibir uma caixa de diálogo que permita ao usuário selecionar o armazenamento a ser aberto. Uma caixa de diálogo pode ser necessária, por exemplo, se um servidor foi renomeado, um nome de conta foi alterado ou partes da rede não estão disponíveis.
  
Quando  _lpEntryID_ for **nulo**, o armazenamento de mensagens a ser usado ainda não foi selecionado. O provedor ainda pode acessar um armazenamento sem exibir uma caixa de diálogo se ele oferece suporte a outros métodos para especificar o armazenamento. Por exemplo, o provedor pode verificar seu arquivo de inicialização ou pode procurar propriedades adicionais que foram colocadas em sua seção de perfil do serviço de mensagens na configuração.
  
Se um provedor achar que todas as informações necessárias não estão no perfil, ele deverá retornar MAPI_E_UNCONFIGURED. MAPI will then call the provider's message service entry point function to enable the user to select a store, or even to create one, and to enter an account name and password, as needed. MAPI automatically creates a new profile section for a new store; essa nova seção de perfil pode ser temporária ou permanente, dependendo de como ela foi adicionada. Se o provedor de armazenamento chamar o método **IMAPISupport::ModifyProfile,** a nova seção de perfil se tornará permanente e o armazenamento será adicionado à lista de armazenamentos de mensagens retornados pelo método [IMAPISession::GetMsgStoresTable.](imapisession-getmsgstorestable.md) 
  
O  _parâmetro lpInterface_ especifica a IID da interface necessária para o objeto de armazenamento recém-aberto. Passar **nulo**  _em lpInterface_ especifica que a interface do repositório de mensagens MAPI, **IMsgStore**, é necessária. Passar o objeto de repositório de mensagens, IID_IMsgStore, também especifica que **iMsgStore** é necessário. Se IID_IUnknown for passado em  _lpInterface_, o provedor deve abrir o repositório usando qualquer interface derivada de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) é melhor para o provedor (novamente, normalmente é **IMsgStore**). Quando IID_IUnknown é passada, a implementação de chamada usa o método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para selecionar uma interface depois que a operação de abertura do armazenamento é bem-sucedida. 
  
A chamada **IMSProvider::Logon** deve retornar informações suficientes, como um caminho para o armazenamento e credenciais para acessar o armazenamento, para permitir que o spooler MAPI faça logon no mesmo armazenamento que o provedor de armazenamento faz sem apresentar uma caixa de diálogo. Os  _parâmetros lpcbSpoolSecurity_  _e lppbSpoolSecurity_ são usados para retornar essas informações. O provedor aloca a memória para esses dados passando um ponteiro para um buffer no parâmetro _lpfAllocateBuffer_ da função [MSProviderInit;](msproviderinit.md) o provedor coloca o tamanho desse buffer em _lpcbSpoolSecurity_. 
  
O MAPI libera esse buffer quando apropriado. Se o logon do spooler MAPI para o armazenamento pode ser realizado apenas a partir das informações na seção de perfil, o provedor pode retornar nulo em  _lppbSpoolSecurity_ e 0 para o tamanho das informações em  _lpcbSpoolSecurity_. O logon do spooler MAPI ocorre como parte de um processo diferente do logon do armazenamento; como o buffer que contém as informações passadas é copiado entre processos, ele pode não estar na memória no mesmo local para o processo do spooler MAPI do processo do provedor de armazenamento. Portanto, um provedor não deve colocar endereços nesse buffer. Para obter mais informações sobre o logon do spooler MAPI, consulte o [método IMSProvider::SpoolerLogon.](imsprovider-spoolerlogon.md) 
  
A maioria dos provedores de armazenamento usa o método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) do objeto de suporte passado no parâmetro  _lpMAPISup_ para salvar e recuperar credenciais e opções do usuário. **OpenProfileSection permite** que um provedor de armazenamento salve informações arbitrárias adicionais em uma seção de perfil e associá-la a um recurso específico. Por exemplo, um provedor de armazenamento pode salvar o nome da conta de usuário e a senha associados a um recurso e quaisquer caminhos ou outras informações necessárias para acessar esse recurso. 
  
Propriedades com identificadores de 0x6600 por meio 0x67FF são propriedades seguras disponíveis para o provedor para seu próprio uso para armazenar dados particulares em seções de perfil. Para obter mais informações sobre os usos de propriedades em objetos de seção de perfil, consulte o [método IProfSect : IMAPIProp.](iprofsectimapiprop.md) 
  
Além de quaisquer dados privados em propriedades com identificadores 0x6600 por meio do 0x67FF, o provedor de armazenamento deve fornecer informações para a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) em sua seção de perfil. Ele deve ser colocado em **PR_DISPLAY_NAME** nome de exibição do próprio provedor — uma cadeia de caracteres de identificação (por exemplo, "Microsoft Personal Information Store") exibida aos usuários para que eles possam distinguir esse armazenamento de mensagens de outros aos quais possam ter acesso. **PR_DISPLAY_NAME** geralmente contém um nome de servidor, um nome de conta de usuário ou um caminho. 
  
Algumas propriedades de seção de perfil são visíveis na tabela do armazenamento de mensagens; outros ficam visíveis durante a instalação, instalação e configuração do subsistema MAPI. O provedor normalmente fornece informações para essas propriedades visíveis para uma nova seção de perfil, que ainda não inclui credenciais salvas ou informações privadas, e quando descobre que essas informações de propriedade foram alteradas. Para obter mais informações sobre seções de perfil, consulte [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
Depois de fazer logor com êxito em um usuário e antes de retornar ao MAPI, o provedor de armazenamento deve criar a matriz de propriedades para a linha de status do recurso e chamar o método [IMAPISupport::ModifyStatusRow.](imapisupport-modifystatusrow.md) 
  
 As chamadas de **logon** que abrem os armazenamentos de mensagens que já estão abertos para a sessão MAPI atual ignoram grande parte do processamento descrito anteriormente. Essas chamadas não criam linhas de status, retornam objetos de logon do armazenamento de mensagens, chamam **AddRef** para o objeto de suporte MAPI ou retornam dados para logon do spooler MAPI. Essas chamadas retornam S_OK e retornam um objeto de armazenamento de mensagens com a interface solicitada. 
  
Para detectar essas chamadas, o provedor deve manter uma lista no objeto do provedor de armazenamento de mensagens dos armazenamentos já abertos para esse objeto de provedor. Ao processar uma **chamada de Logon,** o provedor deve verificar essa lista de lojas abertas e determinar se o armazenamento ao qual fazer logon já está aberto. Se for, as credenciais do usuário não precisam ser verificadas e a exibição de uma caixa de diálogo deve ser evitada, se possível. Se as caixas de diálogo devem ser exibidas, o provedor deve verificar as informações retornadas para ver se um armazenamento foi aberto uma segunda vez. Além disso, o provedor deve verificar se há aberturas duplicadas usando  _lpEntryID_ no início do processamento de **chamada** de logon. 
  
O processamento padrão para uma **chamada de Logon** que acessa um armazenamento aberto é o seguinte: 
  
1. O provedor de armazenamento chama **AddRef** para o objeto de armazenamento existente se a nova interface que está sendo solicitada for a mesma que a interface para o armazenamento existente. Caso contrário, ele **chamará QueryInterface** para obter a nova interface. Se o armazenamento não suportar a nova interface, o provedor deverá retornar o valor de erro MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. O provedor retorna um ponteiro para a interface necessária do objeto de armazenamento existente  _em lppMDB_.
    
3. O provedor retorna **nulo**  _em lppMSLogon_.
    
4. O provedor não deve abrir o perfil do objeto de suporte passado na chamada. Além disso, ele não deve registrar um identificador exclusivo do provedor, registrar uma linha de status ou retornar dados de logon do spooler MAPI.
    
5. O provedor não deve chamar **AddRef para** o objeto de suporte, porque ele não exige um ponteiro para o objeto. 
    
Sempre que possível, os provedores devem retornar as cadeias de caracteres de erro e aviso apropriadas para chamadas de **Logon,** pois isso facilita bastante a carga dos usuários ao determinar por que algo não funcionou. Para retornar essas cadeias de caracteres, um provedor define os membros na **estrutura MAPIERROR.** O MAPI procura, usa e libera a estrutura **MAPIERROR** se ela for retornada por um provedor. 
  
A memória para **essa estrutura MAPIERROR** deve ser alocada usando o buffer passado em _lpfAllocateBuffer_ na **chamada MSProviderInit.** Quaisquer sequências de caracteres de erro contidas na estrutura retornada deverão estar no formato Unicode se MAPI_UNICODE estiver definida no **logon** _ulFlags;_ caso contrário, elas deverão estar no conjunto de caracteres ANSI. 
  
Para a maioria dos valores de erro **retornados de Logon,** o MAPI desabilita os serviços de mensagem aos quais o provedor com falha pertence. O MAPI não chamará nenhum provedor que pertença a esses serviços durante a sessão MAPI. Por outro lado, quando **Logon** retorna o valor MAPI_E_FAILONEPROVIDER de erro de seu logon, o MAPI não desabilita o serviço de mensagens ao qual o provedor pertence. **O logon** deve MAPI_E_FAILONEPROVIDER se encontrar um erro que não garante a desabilitação de todo o serviço durante a sessão. Por exemplo, um provedor pode retornar esse erro quando não permitir a exibição de uma interface do usuário e uma senha necessária não estiver disponível. 
  
Se um provedor retornar MAPI_E_UNCONFIGURED de seu logon, o MAPI chamará a função de entrada do serviço de mensagens do provedor e repetirá o logon. O MAPI MSG_SERVICE_CONFIGURE como o contexto para dar ao serviço uma chance de se configurar. Se o cliente tiver optado por permitir uma interface do usuário no logon, o serviço poderá apresentar sua folha de propriedades de configuração para que o usuário possa inserir informações de configuração.
  
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

