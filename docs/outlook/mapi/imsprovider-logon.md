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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9c7f62c69c7a06f7ca0e4bfddcf789cddc536ea6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386562"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Logs de MAPI em uma instância de um provedor de armazenamento de mensagem.
  
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
  
> [in] Um ponteiro para MAPI atual suporte ao objeto para o armazenamento de mensagens.
    
 _ulUIParam_
  
> [in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe. 
    
 _lpszProfileName_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém o nome do perfil que está sendo usado para logon de provedor de repositório. Esta cadeia de caracteres pode ser exibida nas caixas de diálogo, gravada em um arquivo de log ou simplesmente ignorada. Ele deve estar no formato Unicode, se o sinalizador MAPI_UNICODE é definido no parâmetro _ulFlags_ . 
    
 _cbEntryID_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada para o armazenamento de mensagens. Passando _lpEntryID_ **Nulo** indica que um armazenamento de mensagens ainda não foi selecionado e que as caixas de diálogo que permitem que o usuário selecione um armazenamento de mensagens podem ser apresentadas. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o logon é executado. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> A chamada será autorizada tenha êxito, mesmo se o objeto subjacente não está disponível para a implementação de chamada. Se o objeto não estiver disponível, uma chamada subsequente ao objeto pode gerar um erro.
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se MAPI_UNICODE não estiver definida, as cadeias de caracteres estão no formato ANSI.
    
MDB_NO_DIALOG 
  
> Impede a exibição das caixas de diálogo de logon. Se esse sinalizador estiver definido, o valor de erro MAPI_E_LOGON_FAILED retornado se o logon for bem sucedido. Se esse sinalizador não estiver definido, o provedor de armazenamento de mensagens pode solicita ao usuário para corrigir um nome ou a senha, insira um disco ou para executar outras ações que são necessárias para estabelecer a conexão para o repositório.
    
MDB_NO_MAIL 
  
> O armazenamento de mensagens não deve ser usado para envio ou recebimento de email. O sinalizador sinaliza MAPI não para notificar o spooler MAPI que este armazenamento de mensagens está sendo aberto. Se esse sinalizador estiver definido e o armazenamento de mensagens está firmemente combinado com um provedor de transporte, o provedor não precisará chamar o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) . 
    
MDB_TEMPORARY 
  
> Logs no repositório de forma que as informações podem ser recuperadas por meio de programação, na seção perfil, sem usam das caixas de diálogo. Esse sinalizador instrui o MAPI que o repositório não deve ser adicionado à tabela do repositório de mensagens e que o repositório não pode ser feito permanente. Se esse sinalizador estiver definido, os provedores de armazenamento de mensagem não precisará chamar o método [IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md) . 
    
MDB_WRITE 
  
> Permissão de leitura/gravação solicitações.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) para o armazenamento de mensagens fazer logon. Passar **Nulo** indica que a interface MAPI para o armazenamento de mensagens ( [IMsgStore](imsgstoreimapiprop.md)) é retornada. O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriado para o armazenamento de mensagens (por exemplo, IID_IUnknown ou IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> [out] Um ponteiro para a variável em que o provedor de armazenamento retorna o tamanho, em bytes, dos dados de validação no parâmetro _lppbSpoolSecurity_ . 
    
 _lppbSpoolSecurity_
  
> [out] Um ponteiro para o ponteiro para os dados retornados de validação. Esses dados de validação são fornecidos para que o método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) pode efetuar o MAPI spooler no mesmo armazenamento como o provedor de armazenamento de mensagem. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a retornado [MAPIERROR](mapierror.md) estrutura, se houver, que contém informações de versão, componente e contexto para um erro. O parâmetro _lppMAPIError_ pode ser definido como **null** se não houver nenhuma estrutura **MAPIERROR** para retornar. 
    
 _lppMSLogon_
  
> [out] Um ponteiro para o ponteiro para a mensagem armazenar o objeto de logon de MAPI fazer logon.
    
 _lppMDB_
  
> [out] Um ponteiro para o ponteiro para a mensagem armazenar o objeto para o spooler MAPI e os aplicativos de cliente para fazer logon.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_FAILONEPROVIDER 
  
> Esse provedor não pode fazer logon, mas esse erro não deve desabilitar o serviço. 
    
MAPI_E_LOGON_FAILED 
  
> Não foi possível estabelecer uma sessão de logon.
    
MAPI_E_UNCONFIGURED 
  
> O perfil não conter informações suficientes para que o logon concluir. Quando este valor é retornado, MAPI chama a função do ponto de entrada de serviço de mensagem do provedor de repositório a mensagem.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
MAPI_E_UNKNOWN_CPID 
  
> O servidor não está configurado para oferecer suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> O servidor não está configurado para oferecer suporte a informações de localidade do cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas o provedor de armazenamento de mensagem tem informações de erro disponíveis. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md). Para obter as informações de erro do provedor, chame o método [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Comentários

MAPI chama o método **IMSProvider::Logon** para fazer a maior parte do processamento necessário para obter acesso a um armazenamento de mensagens. Provedores de armazenamento de mensagem validam as credenciais de usuário necessárias para acessar um repositório específico e retornar um objeto de repositório de mensagem no parâmetro _lppMDB_ que os aplicativos de cliente e o spooler MAPI podem fazer logon em. 
  
Além do objeto de repositório de mensagem retornada para o cliente e o uso de spooler MAPI, o provedor também retorna um objeto de logon do repositório de mensagem para MAPI usar em controlar o repositório aberto. O objeto de logon do repositório de mensagem e o objeto de repositório de mensagem devem ser estreitamente vinculadas dentro do provedor de armazenamento de mensagem para que cada uma pode afetar o outro. O uso do objeto store e o objeto de logon deve ser idêntico; deve haver uma correspondência direta entre o objeto de logon e o objeto de armazenamento, de forma que os objetos agir como se fossem um objeto que expõe duas interfaces. Os dois objetos também é preciso criar juntas e liberação juntos. 
  
O objeto de suporte MAPI, criado pelo MAPI e passadas para o provedor no parâmetro _lpMAPISup_ , fornece acesso às funções no MAPI que requer que o provedor. Eles incluem funções que salvar e recuperar informações de perfil, acessar os catálogos de endereços e assim por diante. O ponteiro _lpMAPISup_ pode ser diferente para cada repositório que é aberto. Enquanto o processamento de chamadas para um armazenamento de mensagens após o logon, o provedor de armazenamento deve usar a variável de _lpMAPISup_ que é específica para esse repositório. Qualquer chamada de **Logon** que abre um armazenamento de mensagens e tiver êxito na criação de um objeto de logon do repositório de mensagem, o provedor deve salvar um ponteiro para o objeto de suporte MAPI no objeto de logon repositório e deve chamar o método [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para adicionar uma referência para o objeto de suporte. 
  
O parâmetro _ulUIParam_ deve ser usado se o provedor apresenta caixas de diálogo durante a chamada de **Logon** . No entanto, as caixas de diálogo não devem ser apresentadas se _ulFlags_ contiver o sinalizador MDB_NO_DIALOG. Se uma interface de usuário precisa ser chamado, mas não é permitir que _ulFlags_ , ou se por algum outro motivo uma interface de usuário não pode ser exibida, o provedor deve retornar MAPI_E_LOGON_FAILED. Se o **Logon** exibe uma caixa de diálogo e o usuário cancela o logon, geralmente clicando o botão **Cancelar** da caixa de diálogo, o provedor deve retornar MAPI_E_USER_CANCEL. 
  
O parâmetro _lpEntryID_ pode ser **Nulo** ou apontar para um repositório desfeita entrada identificador que armazenam essa mensagem criado anteriormente. Se _lpEntryID_ aponta para um identificador de entrada desfeita, esse identificador de entrada pode ser provenientes de um dos vários lugares: 
  
- Pode ser um identificador de entrada que o provedor de armazenamento anteriormente quebrado automaticamente e escreveu para a seção de perfil como uma propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
- Pode ser um identificador de entrada que o provedor anteriormente quebrado automaticamente e retornados a um cliente da chamada como uma propriedade **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). 
    
- Pode ser um identificador de entrada que o provedor anteriormente quebrado automaticamente e retornados para um cliente da chamada como a propriedade **PR_ENTRYID** de um objeto de repositório de mensagem. 
    
Em qualquer um desses casos, é possível que o identificador de entrada foi criado em um computador diferente daquele usado no momento.
  
Quando _lpEntryID_ não for **nula**, ele deve conter todas as informações necessárias para identificar e localizar o armazenamento de mensagens. Essas informações podem incluir nomes de volume de rede, números de telefone, nomes de conta de usuário e assim por diante. Se a conexão para o repositório não pode ser feita usando os dados do identificador de entrada, o provedor de armazenamento deve exibir uma caixa de diálogo que permite ao usuário selecionar o repositório a ser aberto. Uma caixa de diálogo pode ser necessária, por exemplo, se um servidor foi renomeado, um nome de conta foi alterada ou partes da rede não estão disponíveis.
  
Quando _lpEntryID_ é **Nulo**, o armazenamento de mensagens para usar ainda não foi selecionado. O provedor ainda pode acessar um repositório sem exibir uma caixa de diálogo se dá suporte a métodos adicionais para especificar o repositório. Por exemplo, o provedor pode verificar seu arquivo de inicialização, ou ele pode procurar propriedades adicionais que foram colocadas na seção de perfil do seu ou seu serviço de mensagem em configuração.
  
Se um provedor localiza que todas as informações necessárias não estão no perfil, ele deverá retornar MAPI_E_UNCONFIGURED. MAPI chamará função do ponto de entrada do provedor a mensagem service para permitir que o usuário para selecionar um repositório, ou até mesmo para criar um e inserir um nome de conta e senha, como necessária. MAPI cria automaticamente uma nova seção de perfil para um novo repositório; Essa nova seção perfil pode ser temporário ou permanente, dependendo de como ela foi adicionada. Se o provedor de armazenamento chama o método **IMAPISupport::ModifyProfile** , nova seção perfil se torna permanente e o repositório for adicionado à lista de armazenamentos de mensagens retornadas pelo método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
O parâmetro _lpInterface_ Especifica o IID da interface necessária para o objeto store recém-aberta. Passando **Nulo** _lpInterface_ Especifica que a interface de repositório de mensagem MAPI, **IMsgStore**, é necessária. Passar o objeto de repositório de mensagem, IID_IMsgStore, também especifica que **IMsgStore** é necessária. Se IID_IUnknown é transmitido em _lpInterface_, o provedor deve abrir o repositório usando qualquer interface derivada de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) é mais adequado para o provedor (novamente, isso é geralmente **IMsgStore**). Quando IID_IUnknown é passado, a implementação chamando usa o método de [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para selecionar uma interface após a operação de abertura do repositório for bem-sucedido. 
  
A chamada **IMSProvider::Logon** deve retornar informações suficientes, por exemplo, um caminho para o repositório e as credenciais para acessar o repositório, para permitir que o spooler MAPI fazer logon no repositório mesmo que o provedor de armazenamento faz sem apresentar uma caixa de diálogo. Os parâmetros _lpcbSpoolSecurity_ e _lppbSpoolSecurity_ são usados para retornar essas informações. O provedor aloca a memória para esses dados ao passar um ponteiro para um buffer no parâmetro de _lpfAllocateBuffer_ da função [MSProviderInit](msproviderinit.md) ; o provedor coloca o tamanho desse buffer na _lpcbSpoolSecurity_. 
  
MAPI libera esse buffer quando apropriado. Se o logon do spooler MAPI para o repositório pode ser realizado com as informações na seção perfil sozinha, o provedor pode retornar null no _lppbSpoolSecurity_ e 0 para o tamanho da informação em _lpcbSpoolSecurity_. Fazer logon MAPI spooler ocorre como parte de um processo diferente do repositório de logon; porque o buffer que contém as informações passadas obtém copiado entre processos, talvez não seja na memória no mesmo local para o processo de spooler MAPI que para o processo de provedor de armazenamento. Portanto, um provedor não deve colocar o endereços nesse buffer. Para obter mais informações sobre o logon do MAPI spooler, consulte o método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) . 
  
A maioria dos provedores de repositório use o método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) do objeto suporte passado no parâmetro _lpMAPISup_ para a salvando e recuperando opções e as credenciais do usuário. **OpenProfileSection** permite que um provedor de armazenamento salvar informações arbitrárias adicionais em uma seção de perfil e associá-lo a um determinado recurso. Por exemplo, um provedor de armazenamento pode salvar o nome da conta de usuário e a senha associada a um recurso e todos os caminhos ou outras informações necessárias para acessar o recurso. 
  
Propriedades com identificadores de propriedade 0x6600 por meio de 0x67FF são seguras propriedades disponíveis para o provedor para seu próprio uso armazenar dados particulares nas seções de perfil. Para obter mais informações sobre os usos das propriedades nos objetos de seção de perfil, consulte o [IProfSect: IMAPIProp](iprofsectimapiprop.md) método. 
  
Além de quaisquer dados particulares nas propriedades com identificadores 0x6600 por meio de 0x67FF, o provedor de armazenamento deverão fornecer informações para a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) em sua seção de perfil. Deve colocar em **PR_DISPLAY_NAME** o nome de exibição do próprio provedor — uma sequência de identificação (por exemplo, "Microsoft Personal Information Store") que será exibida aos usuários para que eles possam distinguir este armazenamento de mensagens de outras pessoas podem ter acessarem Para. **PR_DISPLAY_NAME** comumente contém um nome de servidor, o nome da conta de usuário ou o caminho. 
  
Algumas propriedades da seção de perfil estão visíveis na tabela de repositório de mensagens; outros estão visíveis durante a instalação, instalação e configuração do subsistema de MAPI. O provedor geralmente fornece informações para essas propriedades visíveis ambas para uma nova seção de perfil, que ainda não inclui credenciais salvas ou informações particulares e quando encontrar informações sobre a propriedade mudou. Para obter mais informações sobre as seções de perfil, consulte [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
Após efetuar o logon em um usuário e antes de retornar à MAPI, o provedor de armazenamento deve criar a matriz de propriedades para a linha de status do recurso e chame o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . 
  
 Chamadas de **logon** que abrir armazenamentos de mensagem que já estão abertos para a sessão MAPI atual ignorar grande parte do processamento descrito anteriormente. Essas chamadas não criar linhas de status, retornam objetos de logon do repositório de mensagem, **AddRef** de chamada para o objeto de suporte MAPI ou retornar dados de logon do spooler MAPI. Essas chamadas retornar S_OK e retornar um objeto de repositório de mensagem com a interface solicitada. 
  
Para detectar dessas chamadas, o provedor deve manter uma lista em que o objeto de provedor de armazenamento de mensagem dos repositórios já aberto para este objeto de provedor. Durante o processamento de uma chamada de **Logon** , o provedor deve examinar esta lista dos repositórios open e determinar se o repositório de logon já está aberto. Se for, as credenciais do usuário não precisa ser verificado e a exibição de uma caixa de diálogo deve ser evitada, se possível. Se as caixas de diálogo devem ser exibidas, o provedor deve verificar as informações retornadas para ver se um repositório foi aberto uma segunda vez. Além disso, o provedor deve verificar aberturas duplicadas, usando _lpEntryID_ no início da chamada de **Logon** de processamento. 
  
Padrão de processamento de uma chamada de **Logon** que acessa um armazenamento open é da seguinte maneira: 
  
1. O provedor de armazenamento chama **AddRef** para o objeto de repositório existente, se a nova interface que está sendo solicitada é o mesmo que a interface para o repositório existente. Caso contrário, ele chama **QueryInterface** para obter a nova interface. Se o repositório não der suporte a nova interface, o provedor deve retornar o valor de erro MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. O provedor retorna um ponteiro para a interface necessária do objeto store existente na _lppMDB_.
    
3. O provedor retornará **null** no _lppMSLogon_.
    
4. O provedor não deve abrir o perfil para o objeto de suporte passado na chamada. Além disso, ele deve não registrar um identificador exclusivo do provedor, registrar uma linha de status ou retornar dados de logon de spooler MAPI.
    
5. O provedor não deve chamar **AddRef** para o objeto de suporte, pois ele não requer um ponteiro para o objeto. 
    
Sempre que possível, provedores devem retornar o erro apropriado e o aviso de cadeias de caracteres para chamadas de **Logon** , porque isso significativamente alivia a carga de usuários na determinação por que algo não funcionou. Para retornar essas cadeias de caracteres, um provedor define os membros na estrutura **MAPIERROR** . MAPI procura, usa e libera a estrutura **MAPIERROR** quando é retornado por um provedor. 
  
Deve ser alocar memória para essa estrutura **MAPIERROR** usando o buffer passado na chamada **MSProviderInit** _lpfAllocateBuffer_ . Qualquer erro cadeias de caracteres contidas na estrutura retornada devem estar no formato Unicode se MAPI_UNICODE for definida no **Logon** _ulFlags;_ caso contrário, eles devem estar no caractere ANSI definidos. 
  
Para a maioria dos valores de erro retornados de **Logon**, MAPI desabilita os serviços de mensagem ao qual pertence o provedor está falhando. MAPI não chamará qualquer provedor que pertencem a esses serviços por toda a duração da sessão MAPI. Por outro lado, quando o **Logon** retornará o valor de erro MAPI_E_FAILONEPROVIDER do seu logon, MAPI não desabilite o serviço de mensagem ao qual o provedor pertence. **Logon** deve retornar MAPI_E_FAILONEPROVIDER se encontra um erro dizendo que não garantem a desabilitar todo o serviço por toda a duração da sessão. Por exemplo, um provedor pode retornar esse erro quando ele não permite a exibição de uma interface de usuário e uma senha necessária não está disponível. 
  
Se um provedor retorna MAPI_E_UNCONFIGURED de seu logon, MAPI será chamada de função de entrada de serviço de mensagem do provedor e tente novamente o logon. MAPI passa MSG_SERVICE_CONFIGURE como contexto para dar o serviço a oportunidade de se configurar. Se o cliente tiver escolhido permitir que uma interface de usuário de fazer logon, o serviço pode representar sua folha de propriedades de configuração para que o usuário pode digitar informações de configuração.
  
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

